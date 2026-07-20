# BASIC: Get client metadata document

Retrieves a client metadata document from BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-client-metadata-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-client-metadata-document?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-client-metadata-document?${params}`, {
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
      "application_type": "string",
      "client_id": "string",
      "client_name": "Ava Chen",
      "client_uri": "string",
      "grant_types": [
        [
          "string"
        ]
      ],
      "logo_uri": "string",
      "redirect_uris": [
        [
          "string"
        ]
      ],
      "response_types": [
        [
          "string"
        ]
      ],
      "schema": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application_type` | string |  |
| `client_id` | string |  |
| `client_name` | string |  |
| `client_uri` | string |  |
| `grant_types[]` | array<string> |  |
| `logo_uri` | string |  |
| `redirect_uris[]` | array<string> |  |
| `response_types[]` | array<string> |  |
| `schema` | object |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /projects/{id}/client-metadata.json` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client-metadata-document.md) for the provider-specific parameters and requirements.

