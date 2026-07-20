# Rossum: Retrieve Upload

Retrieves an upload from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-upload?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-upload?${params}`, {
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
| `uploadID` | string | no | Rossum upload ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotations": [
        "string"
      ],
      "createdAt": "string",
      "creator": "string",
      "documents": [
        "string"
      ],
      "email": {},
      "id": 1,
      "organization": "string",
      "queue": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotations[]` | string |  |
| `createdAt` | string |  |
| `creator` | string |  |
| `documents[]` | string |  |
| `email` | object |  |
| `id` | number |  |
| `organization` | string |  |
| `queue` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `GET /uploads/:uploadID` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-upload.md) for the provider-specific parameters and requirements.

