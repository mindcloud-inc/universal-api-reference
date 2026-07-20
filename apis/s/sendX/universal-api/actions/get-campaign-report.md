# SendX: Get Campaign Report



```
GET https://connect.mindcloud.co/v1/universal/sendX/latest/actions/get-campaign-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendX/latest/actions/get-campaign-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendX/latest/actions/get-campaign-report?${params}`, {
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
| `identifier` | string | no | The SendX campaign identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounceContactCount": 1,
      "campaign": "string",
      "clickedContactCount": 1,
      "clickedUniqueContactCount": 1,
      "linkStats": {},
      "openedContactCount": 1,
      "openedUniqueContactCount": 1,
      "repliedContactCount": 1,
      "sentContactCount": 1,
      "spamContactCount": 1,
      "unsubscribeContactCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounceContactCount` | number |  |
| `campaign` | string |  |
| `clickedContactCount` | number |  |
| `clickedUniqueContactCount` | number |  |
| `linkStats` | object |  |
| `openedContactCount` | number |  |
| `openedUniqueContactCount` | number |  |
| `repliedContactCount` | number |  |
| `sentContactCount` | number |  |
| `spamContactCount` | number |  |
| `unsubscribeContactCount` | number |  |

## Native endpoint

Through the native SendX API, this operation is `GET /report/campaign/:identifier` (base URL `https://api.sendx.io/api/v1/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-report.md) for the provider-specific parameters and requirements.

