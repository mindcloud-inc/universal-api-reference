# IntakeQ: List Client Files

Retrieves client files from IntakeQ.

```
GET https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/list-client-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/list-client-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/list-client-files?${params}`, {
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
      "contentType": "string",
      "dateCreated": 1,
      "fileName": "Ava Chen",
      "folderId": "string",
      "id": "string",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `dateCreated` | number |  |
| `fileName` | string |  |
| `folderId` | string |  |
| `id` | string |  |
| `size` | number |  |

## Native endpoint

Through the native IntakeQ API, this operation is `GET /files` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-client-files.md) for the provider-specific parameters and requirements.

