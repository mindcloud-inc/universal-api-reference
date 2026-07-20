# SqlBak: List Destinations

Retrieves destinations from SqlBak.

```
GET https://connect.mindcloud.co/v1/universal/sqlBak/latest/actions/list-destinations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SqlBak `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sqlBak/latest/actions/list-destinations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sqlBak/latest/actions/list-destinations?${params}`, {
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
| `serverId` | number | no | Filter destinations by server ID. |
| `jobId` | number | no | Filter destinations by job ID. |
| `destinationType` | list | no | Filter destinations by destination type. One of: `amazon_s3`, `azure_storage`, `backblaze_b2`, `box`, `dropbox`, `folder`, `ftp`, `google_drive`, `onedrive`, `onedrive_for_business`, `s3_compatible`, `yandex_disk`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "has_more": true,
      "list": [
        {}
      ],
      "page": 1,
      "page_size": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_more` | boolean | Whether another page can be requested. |
| `list` | array<object> | Destinations returned for the current page. |
| `page` | number | Current page number. |
| `page_size` | number | Requested page size. |
| `total` | number | Total matching records. |

## Native endpoint

Through the native SqlBak API, this operation is `GET /destinations` (base URL `https://sqlbak.com/public-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-destinations.md) for the provider-specific parameters and requirements.

