# edatalia Sign Online: List Signature History

Retrieves signature history from edatalia Sign Online.

```
GET https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/list-signature-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a edatalia Sign Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/list-signature-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/list-signature-history?${params}`, {
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
| `limit` | number | no | Maximum number of history items to return. Provider maximum is 100. Default: `50`. |
| `offset` | number | no | Number of history items to skip. |
| `reference` | string | no | Filter history by envelope reference. |
| `documentSetName` | string | no | Filter history by envelope name. |
| `recipientEmail` | string | no | Filter history by recipient email. |
| `onlyCurrentUser` | boolean | no | When true, only return envelopes for the current authenticated user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentSetName": "Ava Chen",
      "downloaded": true,
      "id": "string",
      "itemDateTime": "2026-05-07T12:00:00.000Z",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentSetName` | string |  |
| `downloaded` | boolean |  |
| `id` | string |  |
| `itemDateTime` | date |  |
| `status` | number |  |

## Native endpoint

Through the native edatalia Sign Online API, this operation is `GET /PSC/v40/History` (base URL `https://restapi.firmar.online`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signature-history.md) for the provider-specific parameters and requirements.

