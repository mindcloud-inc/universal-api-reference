# OneMap SG: Check Theme Status

Retrieves the status of a OneMap SG theme.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/check-theme-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/check-theme-status?connectionId=$CONNECTION_ID&queryName=kindergartens&dateTime=2023-06-15T16%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queryName": "kindergartens",
  "dateTime": "2023-06-15T16:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/check-theme-status?${params}`, {
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
| `queryName` | string | yes | The theme query name. Example: `kindergartens`. |
| `dateTime` | string | yes | The date and time to check theme availability for. Example: `2023-06-15T16:00:00.000Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "UpdatedFile": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `UpdatedFile` | boolean |  |

## Native endpoint

Through the native OneMap SG API, this operation is `GET /api/public/themesvc/checkThemeStatus` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-theme-status.md) for the provider-specific parameters and requirements.

