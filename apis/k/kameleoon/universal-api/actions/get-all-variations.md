# Kameleoon: Get all variations



```
GET https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-variations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-variations?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramsIo": "page=1, perPage=20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-variations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paramsIo` | string | yes | Required query object documented by Kameleoon for list endpoints. Example: `page=1, perPage=20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": 1,
      "cssCode": "string",
      "customJson": "string",
      "experimentId": 1,
      "forceNoFlicker": true,
      "id": 1,
      "isJsCodeAfterDomReady": true,
      "jsCode": "string",
      "name": "Ava Chen",
      "personalizationId": 1,
      "prompt": {},
      "promptSource": "string",
      "redirection": {},
      "shadowDom": true,
      "siteId": 1,
      "textInput": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | number |  |
| `cssCode` | string |  |
| `customJson` | string |  |
| `experimentId` | number |  |
| `forceNoFlicker` | boolean |  |
| `id` | number |  |
| `isJsCodeAfterDomReady` | boolean |  |
| `jsCode` | string |  |
| `name` | string |  |
| `personalizationId` | number |  |
| `prompt` | object |  |
| `promptSource` | string |  |
| `redirection` | object |  |
| `shadowDom` | boolean |  |
| `siteId` | number |  |
| `textInput` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Kameleoon API, this operation is `GET variations` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-variations.md) for the provider-specific parameters and requirements.

