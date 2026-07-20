# <img src="https://images.mindcloud.co/apps/icons/yep-code_1774981398245.png" alt="YepCode logo" width="28" height="28"> YepCode: Universal API

Build, run, and manage integration processes and automation code

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/yepCode/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://yepcode.io
- **Vendor API docs:** https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get processes](actions/get-processes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-processes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Execution

| Action | Method | Description |
| --- | --- | --- |
| [Get execution](actions/get-execution.md) | GET | Retrieves details for an execution from YepCode. |
| [Get executions](actions/get-executions.md) | GET | Retrieves a list of executions from YepCode. |
| [Kill execution](actions/kill-execution.md) | PUT | Updates an execution in YepCode by terminating it. |
| [Rerun execution](actions/rerun-execution.md) | POST | Creates a new execution in YepCode from an existing one. |

### Execution Log

| Action | Method | Description |
| --- | --- | --- |
| [Get execution logs](actions/get-execution-logs.md) | GET | Retrieves execution log entries from YepCode. |

### Module

| Action | Method | Description |
| --- | --- | --- |
| [Create module](actions/create-module.md) | POST | Creates a new module in YepCode. |
| [Create module version alias](actions/create-module-version-alias.md) | POST | Creates a module version alias in YepCode. |
| [Delete module](actions/delete-module.md) | DELETE | Deletes an existing module from YepCode. |
| [Get module](actions/get-module.md) | GET | Retrieves details for a module from YepCode. |
| [Get modules](actions/get-modules.md) | GET | Retrieves a list of modules from YepCode. |
| [Publish module version](actions/publish-module-version.md) | POST | Creates a published module version in YepCode. |

### Module Version

| Action | Method | Description |
| --- | --- | --- |
| [Get module versions](actions/get-module-versions.md) | GET | Retrieves module version records from YepCode. |

### Module Version Alias

| Action | Method | Description |
| --- | --- | --- |
| [Get module version alias](actions/get-module-version-alias.md) | GET | Retrieves a module version alias from YepCode. |
| [Get module version aliases](actions/get-module-version-aliases.md) | GET | Retrieves module version aliases from YepCode. |

### Object

| Action | Method | Description |
| --- | --- | --- |
| [Get storage object helper](actions/get-storage-object-helper.md) | GET | Retrieves a storage object from YepCode. |
| [Upload storage object](actions/upload-storage-object.md) | POST | Creates a storage object in YepCode from a file. |
| [Upload storage object raw](actions/upload-storage-object-raw.md) | POST | Creates a storage object in YepCode from raw content. |

### Process

| Action | Method | Description |
| --- | --- | --- |
| [Create process](actions/create-process.md) | POST | Creates a new process in YepCode. |
| [Create process version alias](actions/create-process-version-alias.md) | POST | Creates a process version alias in YepCode. |
| [Delete process](actions/delete-process.md) | DELETE | Deletes an existing process from YepCode. |
| [Execute process async](actions/execute-process-async.md) | POST | Creates an asynchronous process execution in YepCode. |
| [Get process](actions/get-process.md) | GET | Retrieves details for a process from YepCode. |
| [Get processes](actions/get-processes.md) | GET | Retrieves a list of processes from YepCode. |
| [Publish process version](actions/publish-process-version.md) | POST | Creates a published process version in YepCode. |
| [Schedule process](actions/schedule-process.md) | POST | Creates a scheduled process in YepCode. |

### Process Version

| Action | Method | Description |
| --- | --- | --- |
| [Get process versions](actions/get-process-versions.md) | GET | Retrieves process version records from YepCode. |

### Process Version Alias

| Action | Method | Description |
| --- | --- | --- |
| [Get process version alias](actions/get-process-version-alias.md) | GET | Retrieves a process version alias from YepCode. |
| [Get process version aliases](actions/get-process-version-aliases.md) | GET | Retrieves process version aliases from YepCode. |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Get scheduled process](actions/get-schedule.md) | GET | Retrieves a scheduled process from YepCode. |
| [Get scheduled processes](actions/get-schedules.md) | GET | Retrieves a list of scheduled processes from YepCode. |
| [Pause scheduled process](actions/pause-schedule.md) | PUT | Updates a scheduled process in YepCode by pausing it. |
| [Resume scheduled process](actions/resume-schedule.md) | PUT | Updates a scheduled process in YepCode by resuming it. |

### Storage Object

| Action | Method | Description |
| --- | --- | --- |
| [Get storage objects](actions/get-storage-objects.md) | GET | Retrieves storage object records from YepCode. |

### Variable

| Action | Method | Description |
| --- | --- | --- |
| [Create variable](actions/create-variable.md) | POST | Creates a new variable in YepCode. |
| [Delete variable](actions/delete-variable.md) | DELETE | Deletes an existing variable from YepCode. |
| [Get variables](actions/get-variables.md) | GET | Retrieves a list of variables from YepCode. |
| [Update variable](actions/update-variable.md) | PUT | Updates an existing variable in YepCode. |

