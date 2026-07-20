# FBI Most Wanted: List Wanted Records

Retrieves wanted records from FBI Most Wanted.

```
GET https://connect.mindcloud.co/v1/universal/fBIMostWanted/latest/actions/list-wanted-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FBI Most Wanted `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fBIMostWanted/latest/actions/list-wanted-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fBIMostWanted/latest/actions/list-wanted-records?${params}`, {
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
      "caution": "string",
      "description": "string",
      "details": "string",
      "eyes": "string",
      "field_offices": [
        "string"
      ],
      "files": [
        {}
      ],
      "hair": "string",
      "height_max": 1,
      "height_min": 1,
      "images": [
        {}
      ],
      "modified": "2026-05-07T12:00:00.000Z",
      "path": "string",
      "pathId": "string",
      "poster_classification": "string",
      "publication": "2026-05-07T12:00:00.000Z",
      "race": "string",
      "remarks": "string",
      "reward_max": 1,
      "reward_min": 1,
      "reward_text": "string",
      "sex": "string",
      "status": "string",
      "subjects": [
        "string"
      ],
      "title": "string",
      "uid": "string",
      "url": "https://example.com",
      "warning_message": "string",
      "weight_max": 1,
      "weight_min": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caution` | string | Long public caution text when available. |
| `description` | string | Short public description for the wanted record. |
| `details` | string | Long public details text when available. |
| `eyes` | string | Eye color value when available. |
| `field_offices` | array<string> | FBI field offices associated with the record. |
| `files` | array<object> | Downloadable file metadata returned by the API. |
| `hair` | string | Hair value when available. |
| `height_max` | number | Maximum height in inches when available. |
| `height_min` | number | Minimum height in inches when available. |
| `images` | array<object> | Image metadata objects returned by the API. |
| `modified` | date | Last modified timestamp returned by the API. |
| `path` | string | FBI.gov relative path for the record. |
| `pathId` | string | API path identifier for the record. |
| `poster_classification` | string | FBI poster classification for the record. |
| `publication` | date | Publication timestamp returned by the API. |
| `race` | string | Normalized race value when available. |
| `remarks` | string | Additional public remarks when available. |
| `reward_max` | number | Maximum reward amount when available. |
| `reward_min` | number | Minimum reward amount when available. |
| `reward_text` | string | Public reward text when available. |
| `sex` | string | Sex value when available. |
| `status` | string | Public status value returned by the FBI Wanted API. |
| `subjects` | array<string> | FBI wanted categories associated with the record. |
| `title` | string | Wanted record title or person/case name. |
| `uid` | string | Unique FBI Wanted API record identifier. |
| `url` | string | Public FBI.gov wanted-record page URL. |
| `warning_message` | string | Public warning message when available. |
| `weight_max` | number | Maximum weight in pounds when available. |
| `weight_min` | number | Minimum weight in pounds when available. |

## Native endpoint

Through the native FBI Most Wanted API, this operation is `GET /list` (base URL `https://api.fbi.gov/wanted/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-wanted-records.md) for the provider-specific parameters and requirements.

