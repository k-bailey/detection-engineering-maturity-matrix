# detection-engineering-maturity-matrix

Article: https://kyle-bailey.medium.com/detection-engineering-maturity-matrix-f4f3181a5cc7

|            | Defined                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Managed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Optimized                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| People     | <li>Ad-hoc team building/managing detection (i.e. part time IR task) <li>Leadership has basic understanding of detection processes and challenges but limited resources or different priorities may exist <li>SME's in none or very few detection domains (i.e. network, host, etc.)                                                                                                                                                                                                               | <li>Dedicated individuals performing detection work full time <li>Leadership advocates for detection. The size of the team and resources needed may not be fully understood <li>SME’s on some tools & log sources, informally defined domain ownership                                                                                                                                                                                                                                                                                                                                                    | <li>Dedicated team with defined SME's for all detection domains (host, network, application, cloud, etc.) <li>Leadership advocates for involvement in detection processes across the org, as well as necessary tools, licensing and staffing                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Processes  | <li>Detection strategy and workflow are not well documented or defined <li>Detection quality depends greatly on the understanding of the individual performing the work <li>No backlog or prioritization of known gaps <li>Little or no active maintenance or monitoring of existing detection <li>Little to no detection related metrics                                                                                                                                                         | <li>Detection strategy and workflow are defined and followed <li>Approval and handoff processes are loosely defined  <li>Work is prioritized in an ad-hoc way with little to no input from threat intel or others <li>Maintenance and monitoring is performed but is ad-hoc and generally done reactively  <li>Some metrics exist for categories such as fidelity, MTTD, and automated resolutions                                                                                                                                                                                                          | <li>Detection strategy is continuously iterated on <li>Defined review and approval processes exist for new and updated detection, and IR is given final approval permissions <li>Work is prioritized by input from threat intel, and technology SME's <li>Maintenance and monitoring is continuous and most issues are identified proactively <li>KPI's are well defined to include applicable Mitre Att&ck coverage per environment (i.e. Win, Mac, Corp, Prod, etc.)                                                                                                                                                                                                                                                                                                                                                  |
| Technology | <li>Visibility is inconsistent and some sources critical for custom detection may be missing <li>Timeliness of log sources is not tracked <li>Little to no detection-as-code principles are followed <li>No alerts are continuously tested to ensure they are functional                                                                                                                                                                                                                          | <li>Most critical log sources are available in the SIEM. Some log health alerting exists. <li>Most log sources are timely (< 5-10 min) <li>Some detection as code principles are followed <li>Few alerts are continuously tested, telemetry from other sources are alerted on (SIEM errors, log health)                                                                                                                                                                                                                                                                                                      | <li>Detection defines critical log sources and ensures they are present in the SIEM. Log health is tracked and alerted on <li>Detection as code is engrained in the team, version control, review and approval, static, dynamic and continuous testing are baked into the deployment pipeline <li>Almost all detection logic is continuously tested in an automated way                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Detection  | <li>Most detection creation is reactive to incidents or near misses <li>Detection is tied loosely to Mitre Att&ck, but there is no formal tracking <li>Threats are emulated by the detection individuals themselves or using historical data, no active red/purple teaming occurs <li>Detection is primarily indicator focused, few behavioral TTP detections exist <li>All detection logic is treated equal in priority <li>All alerts must be manually reviewed and interacted with by the IR team | <li>Detection creation is more proactive and prioritized loosely on threat intel (known, likely threats) <li>Mitre Att&ck TTP's a detection use-case covers are documented but aggregation of coverage may be manual <li>Reactive purple team exercises occur, potentially loosely driven by threat intel <li>More behavioral based detections exist, new detection is mostly TTP focused (where possible)  <li>Some high fidelity, high impact detection logic runs in near real time and priority is communicated to IR <li>The team has some capability to send alerts to end-users for resolution | <li>Detection creation is proactively prioritized based on known and active threats to the org as identified by threat intel with risk input from other teams (i.e Security engineering, architecture, risk) <li>All use-cases are documented with Att&ck TID's and this data can be programmatically retrieved to calculate metrics <li>PurpleTeam exercises are constantly run to validate and improve detection capabilities   <li>Focused primarily on behavioral/TTP detection logic. ML based detection is applied where applicable <li>High fidelity, high impact detection logic runs in near real time and priority is effectively presented to the IR team <li>All alerts where the end-user has context are directed to them. New alerts are constantly questioned for the potential for automated/end-user resolution |
