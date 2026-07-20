# SeekTable: Get Cube Info

Retrieves a SeekTable cube by cube ID.

```
GET https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/get-cube-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeekTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/get-cube-info?connectionId=$CONNECTION_ID&cubeId=d4c32c684cbe42d6abc1392dc42ab028" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cubeId": "d4c32c684cbe42d6abc1392dc42ab028"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/get-cube-info?${params}`, {
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
| `cubeId` | string | yes | GUID of the cube in your SeekTable account. Example: `d4c32c684cbe42d6abc1392dc42ab028`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CanAddReport": true,
      "CanDownloadDataFile": true,
      "CanEditSchema": true,
      "CanMoveReportUpstream": true,
      "CanSearch": true,
      "CanShareToTeam": true,
      "CreateDate": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "Name": "Ava Chen",
      "PivotFilterSuggestWithHint": true,
      "Shared": true,
      "SourceFile": "string",
      "SourceType": "string",
      "SourceTypeId": "string",
      "UpdateDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CanAddReport` | boolean |  |
| `CanDownloadDataFile` | boolean |  |
| `CanEditSchema` | boolean |  |
| `CanMoveReportUpstream` | boolean |  |
| `CanSearch` | boolean |  |
| `CanShareToTeam` | boolean |  |
| `CreateDate` | date |  |
| `Id` | string | GUID of the cube. |
| `Name` | string | Cube name. |
| `PivotFilterSuggestWithHint` | boolean |  |
| `Shared` | boolean |  |
| `SourceFile` | string | Original CSV source file name. |
| `SourceType` | string | Human-readable source type label. |
| `SourceTypeId` | string | Machine-readable source type identifier. |
| `UpdateDate` | date |  |

## Native endpoint

Through the native SeekTable API, this operation is `GET /api/cube/:cube_id` (base URL `https://www.seektable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cube-info.md) for the provider-specific parameters and requirements.

