# RD Station Marketing: List Segmentations



```
GET https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-segmentations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-segmentations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-segmentations?${params}`, {
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
      "segmentations": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "links": [
            {
              "href": "https://example.com"
            }
          ],
          "name": "Ava Chen",
          "processStatus": "string",
          "standard": true,
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `segmentations[].createdAt` | date |  |
| `segmentations[].id` | number |  |
| `segmentations[].links[].href` | string |  |
| `segmentations[].name` | string |  |
| `segmentations[].processStatus` | string |  |
| `segmentations[].standard` | boolean |  |
| `segmentations[].updatedAt` | date |  |

## Native endpoint

Through the native RD Station Marketing API, this operation is `GET /platform/segmentations` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segmentations.md) for the provider-specific parameters and requirements.

