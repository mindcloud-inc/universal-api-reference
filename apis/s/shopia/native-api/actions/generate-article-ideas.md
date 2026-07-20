# Generate Article Ideas with Shopia

## Endpoint

- **Method:** `POST`
- **Path:** `https://automation-run-1he1fvca.uc.gateway.dev/automation?key={apiKey}&token={token}&workflow={workflowId}`
- **Base URL:** `https://automation-run-1he1fvca.uc.gateway.dev`
- **Official documentation:** [Generate Article Ideas](https://docs.axelerate.ai/en/articles/9553232-using-the-automations-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputs.Topic` | body | `string` | yes | The topic to generate article ideas about. |
| `inputs.Audience` | body | `string` | yes | The target audience for the article ideas. |
