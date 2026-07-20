# Docage: List Organizations

Retrieves accessible organizations from Docage.

```
GET https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-organizations?${params}`, {
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
      "Address1": "string",
      "City": "string",
      "Country": "string",
      "IntegratorId": "string",
      "IsDemo": true,
      "IsDeveloper": true,
      "Language": 1,
      "Name": "Ava Chen",
      "OrganizationStatus": 1,
      "OrganizationType": 1,
      "Phone": "string",
      "State": "string",
      "ZipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address1` | string |  |
| `City` | string |  |
| `Country` | string |  |
| `IntegratorId` | string |  |
| `IsDemo` | boolean |  |
| `IsDeveloper` | boolean |  |
| `Language` | number |  |
| `Name` | string |  |
| `OrganizationStatus` | number |  |
| `OrganizationType` | number |  |
| `Phone` | string |  |
| `State` | string |  |
| `ZipCode` | string |  |

## Native endpoint

Through the native Docage API, this operation is `GET /Organizations` (base URL `https://api.docage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

