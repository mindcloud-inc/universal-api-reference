# OneMap SG: Retrieve Theme Within Extents

Retrieves OneMap SG theme data within map extents.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/retrieve-theme-within-extents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/retrieve-theme-within-extents?connectionId=$CONNECTION_ID&queryName=dengue_cluster&extents=1.291789%2C103.7796402%2C1.3290461%2C103.8726032" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queryName": "dengue_cluster",
  "extents": "1.291789,103.7796402,1.3290461,103.8726032"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/retrieve-theme-within-extents?${params}`, {
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
| `queryName` | string | yes | The theme query name. Example: `dengue_cluster`. |
| `extents` | string | yes | The bounding box extents as four comma-separated values. Example: `1.291789,103.7796402,1.3290461,103.8726032`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "SrchResults": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `SrchResults` | array<object> |  |

## Native endpoint

Through the native OneMap SG API, this operation is `GET /api/public/themesvc/retrieveTheme` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-theme-within-extents.md) for the provider-specific parameters and requirements.

