# Department of Agriculture: List ARMS Variables

Retrieves ARMS variables from Department of Agriculture.

```
GET https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Department of Agriculture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-variables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-variables?${params}`, {
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
      "abb": "string",
      "desc": "string",
      "group": 1,
      "header": "string",
      "invalid": true,
      "level": 1,
      "report_Num": 1,
      "reportHeader": "string",
      "seq": 1,
      "terms": "string",
      "unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abb` | string | Variable abbreviation. |
| `desc` | string | Variable description. |
| `group` | number | Variable group number. |
| `header` | string | Variable display name. |
| `invalid` | boolean | Whether the variable is invalid. |
| `level` | number | Variable hierarchy level. |
| `report_Num` | number | Report number associated with the variable. |
| `reportHeader` | string | Report name associated with the variable. |
| `seq` | number | Variable sequence. |
| `terms` | string | Provider search terms. |
| `unit` | string | Variable unit. |

## Native endpoint

Through the native Department of Agriculture API, this operation is `GET /arms/variable` (base URL `https://api.ers.usda.gov/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-arms-variables.md) for the provider-specific parameters and requirements.

