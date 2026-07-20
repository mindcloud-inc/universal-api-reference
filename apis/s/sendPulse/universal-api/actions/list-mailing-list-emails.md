# SendPulse: List Mailing List Emails

Retrieves emails from a SendPulse mailing list.

```
GET https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/list-mailing-list-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/list-mailing-list-emails?connectionId=$CONNECTION_ID&mailingListId=123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailingListId": "123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/list-mailing-list-emails?${params}`, {
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
| `mailingListId` | string | yes | The SendPulse mailing list identifier. Example: `123456`. |
| `limit` | number | no | Maximum number of contacts to return. Example: `100`. |
| `offset` | number | no | Number of contacts to skip before returning results. Example: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | boolean | no | Filter to active contacts only. |
| `notActive` | boolean | no | Filter to inactive contacts only. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "add_date": "string",
      "email": "ava@example.com",
      "status": 1,
      "status_explain": "string",
      "variables": {
        "Name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `add_date` | string |  |
| `email` | string |  |
| `status` | number |  |
| `status_explain` | string |  |
| `variables` | object |  |
| `variables.Name` | string |  |

## Native endpoint

Through the native SendPulse API, this operation is `GET /addressbooks/:mailingListId/emails` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mailing-list-emails.md) for the provider-specific parameters and requirements.

