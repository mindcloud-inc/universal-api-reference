# Add Subscriber Attributes with PushAlert

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/web-push/attribute/put`
- **Base URL:** `https://api.pushalert.co`
- **Official documentation:** [Add Subscriber Attributes](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-add-attributes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriber` | body | `string` | yes | Subscriber ID to update. |
| `attributes` | body | `string` | yes | JSON object string of attribute key-value pairs. |
