# Start jobs with UiPath Orchestrator

## Endpoint

- **Method:** `POST`
- **Path:** `/odata/Jobs/UiPath.Server.Configuration.OData.StartJobs`
- **Base URL:** `https://cloud.uipath.com/{organizationName}/{tenantName}/orchestrator_`
- **Official documentation:** [Start jobs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/jobs-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startInfo.ReleaseKey` | body | `string` | yes | The process release key to start. |
| `startInfo.Strategy` | body | `string` | yes | Job start strategy, such as All or Specific. |
| `startInfo.RobotIds[]` | body | `array<number>` | no | Robot IDs for Specific strategy. |
| `startInfo.NoOfRobots` | body | `number` | no | Number of robots to start for robot-count strategies. |
