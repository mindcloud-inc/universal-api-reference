# Federal Communications Commission: Get Entity Access Token

Retrieves an FCC entity access token.

```
GET https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/get-entity-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Communications Commission `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/get-entity-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/get-entity-access-token?${params}`, {
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
| `entityId` | string | no | Unique entity ID. |
| `format` | string | no | Response format. FCC documents json, jsonp, xml. |
| `serviceCode` | string | no | Entity service code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessToken": "string",
      "entityId": "string",
      "serviceCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string | Entity access token returned by the FCC Manager API. |
| `entityId` | string | FCC entity identifier. |
| `serviceCode` | string | FCC service code. |

## Native endpoint

Through the native Federal Communications Commission API, this operation is `POST /api/manager/get/entityAccessToken.{format}` (base URL `https://publicfiles.fcc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-entity-access-token.md) for the provider-specific parameters and requirements.

