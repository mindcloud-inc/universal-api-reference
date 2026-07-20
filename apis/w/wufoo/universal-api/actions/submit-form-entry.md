# Wufoo: Submit Form Entry

Creates a new entry in a specific Wufoo form.

```
POST https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/submit-form-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wufoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/submit-form-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/submit-form-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | The form hash or identifier that will receive the submitted entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entryId": 1,
      "entryLink": "https://example.com",
      "success": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entryId` | number | The created Wufoo entry ID. |
| `entryLink` | string | The Wufoo API link for the created entry. |
| `success` | number | Whether the entry submission succeeded. |

## Native endpoint

Through the native Wufoo API, this operation is `POST /forms/:identifier/entries.json` (base URL `https://{{credentials.subdomain}}.wufoo.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form-entry.md) for the provider-specific parameters and requirements.

