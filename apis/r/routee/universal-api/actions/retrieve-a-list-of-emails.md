# Routee: Retrieve a list of emails

Retrieves a list of emails from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-a-list-of-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-a-list-of-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-a-list-of-emails?${params}`, {
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
| `limit` | string | no | Number of entries |
| `offset` | string | no | Sample offset |
| `from` | string | no | Sample start date |
| `to` | string | no | Sample max date |
| `sender` | string | no | Sender |
| `recipient` | string | no | Recipient |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "recipient": "string",
      "send_date": "string",
      "sender": "string",
      "sender_ip": "string",
      "smtp_answer_code": "string",
      "smtp_answer_data": "string",
      "smtp_answer_subcode": "string",
      "subject": "string",
      "total_size": "string",
      "tracking": {
        "click": 1,
        "client_info": [
          [
            {}
          ]
        ],
        "link": [
          [
            {}
          ]
        ],
        "open": 1
      },
      "used_ip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `recipient` | string |  |
| `send_date` | string |  |
| `sender` | string |  |
| `sender_ip` | string |  |
| `smtp_answer_code` | string |  |
| `smtp_answer_data` | string |  |
| `smtp_answer_subcode` | string |  |
| `subject` | string |  |
| `total_size` | string |  |
| `tracking` | object |  |
| `tracking.click` | number |  |
| `tracking.client_info[]` | array<object> |  |
| `tracking.client_info[].action_date` | string |  |
| `tracking.client_info[].browser` | string |  |
| `tracking.client_info[].country` | string |  |
| `tracking.client_info[].ip` | string |  |
| `tracking.client_info[].os` | string |  |
| `tracking.link[]` | array<object> |  |
| `tracking.link[].action_date` | string |  |
| `tracking.link[].browser` | string |  |
| `tracking.link[].country` | string |  |
| `tracking.link[].ip` | string |  |
| `tracking.link[].os` | string |  |
| `tracking.link[].screen_resolution` | string |  |
| `tracking.link[].url` | string |  |
| `tracking.open` | number |  |
| `used_ip` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /smtp/emails` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-a-list-of-emails.md) for the provider-specific parameters and requirements.

