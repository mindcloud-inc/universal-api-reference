# Zillow MLS Data: Get data systems

Retrieves data systems from Zillow MLS Data.

```
GET https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/get-data-systems
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow MLS Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/get-data-systems?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/get-data-systems?${params}`, {
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
      "DataDictionaryVersion": "string",
      "DateTimeStamp": "2026-05-07T12:00:00.000Z",
      "ID": "string",
      "Name": "Ava Chen",
      "Resources": [
        {}
      ],
      "ServiceURI": "string",
      "TransportVersion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `DataDictionaryVersion` | string | RESO data dictionary version. |
| `DateTimeStamp` | date | Timestamp for the current data-system snapshot. |
| `ID` | string | Unique data-system identifier. |
| `Name` | string | Data system name. |
| `Resources` | array<object> | Resources exposed by the data system. |
| `ServiceURI` | string | Base service URI for the data system. |
| `TransportVersion` | string | Transport version. |

## Native endpoint

Through the native Zillow MLS Data API, this operation is `GET /OData/DataSystem` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-systems.md) for the provider-specific parameters and requirements.

