# Flexmail: List Opt-In Forms

Retrieves opt-in forms from your Flexmail account.

```
GET https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-opt-in-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexmail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-opt-in-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-opt-in-forms?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "language": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | The timestamp when the opt-in form was created. |
| `id` | number | The identifier of the opt-in form. |
| `language` | string | The language of the opt-in form. |
| `name` | string | The display name of the opt-in form. |

## Native endpoint

Through the native Flexmail API, this operation is `GET /opt-in-forms` (base URL `https://api.flexmail.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-opt-in-forms.md) for the provider-specific parameters and requirements.

