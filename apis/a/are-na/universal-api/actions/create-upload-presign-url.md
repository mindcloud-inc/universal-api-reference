# Are.na: Create Upload Presign URL

Creates a presigned upload URL in Are.na.

```
POST https://connect.mindcloud.co/v1/universal/are-na/latest/actions/create-upload-presign-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Are.na `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/create-upload-presign-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/are-na/latest/actions/create-upload-presign-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `files[]` | array<object> | yes | Array of file descriptors with filename and content_type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "fields": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `fields` | object |  |
| `url` | string |  |

## Native endpoint

Through the native Are.na API, this operation is `POST uploads/presign` (base URL `https://api.are.na/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-upload-presign-url.md) for the provider-specific parameters and requirements.

