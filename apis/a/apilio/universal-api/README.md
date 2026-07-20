# <img src="https://images.mindcloud.co/apps/icons/apilio_1776269911634.png" alt="Apilio logo" width="28" height="28"> Apilio: Universal API

Apilio is a smart-home logic platform with a REST API for variables, conditions, and logicblocks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/apilio/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.apilio.com
- **Vendor API docs:** https://documenter.getpostman.com/view/13480928/TzCHAVD2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Boolean Variables](actions/list-boolean-variables.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apilio/latest/actions/list-boolean-variables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Boolean Variable

| Action | Method | Description |
| --- | --- | --- |
| [Get Boolean Variable](actions/get-boolean-variable.md) | GET |  |
| [List Boolean Variables](actions/list-boolean-variables.md) | GET |  |
| [Update Boolean Variable](actions/update-boolean-variable.md) | PUT |  |

### Condition

| Action | Method | Description |
| --- | --- | --- |
| [List Conditions](actions/list-conditions.md) | GET |  |

### Logicblock

| Action | Method | Description |
| --- | --- | --- |
| [Evaluate Logicblock](actions/evaluate-logicblock.md) | PUT |  |
| [List Logicblocks](actions/list-logicblocks.md) | GET |  |
| [Set Logicblock Active State](actions/set-logicblock-active-state.md) | PUT |  |

### Numeric Variable

| Action | Method | Description |
| --- | --- | --- |
| [Get Numeric Variable](actions/get-numeric-variable.md) | GET |  |
| [List Numeric Variables](actions/list-numeric-variables.md) | GET |  |
| [Update Numeric Variable](actions/update-numeric-variable.md) | PUT |  |

### String Variable

| Action | Method | Description |
| --- | --- | --- |
| [Get String Variable](actions/get-string-variable.md) | GET |  |
| [List String Variables](actions/list-string-variables.md) | GET |  |
| [Update String Variable](actions/update-string-variable.md) | PUT |  |

### Time Condition

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Condition](actions/get-time-condition.md) | GET |  |
| [List Time Conditions](actions/list-time-conditions.md) | GET |  |

### Tuya Condition

| Action | Method | Description |
| --- | --- | --- |
| [Get Tuya Condition](actions/get-tuya-condition.md) | GET |  |
| [List Tuya Conditions](actions/list-tuya-conditions.md) | GET |  |

### Variable Condition

| Action | Method | Description |
| --- | --- | --- |
| [Get Variable Condition](actions/get-variable-condition.md) | GET |  |
| [List Variable Conditions](actions/list-variable-conditions.md) | GET |  |

