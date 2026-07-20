# Aspire: Get Workers Comps

Retrieve a list of information related to workers' compensation.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-contact-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-contact-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-contact-types?${params}`, {
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
| `$filter` | string | no | Use filter to refine the conditions that must be met in the data that is returned. In SQL this would be most similar to the WHERE clause. Example: You're searching for Contacts but only want to see the active employees. You might use this filter: "(Active eq true) and (ContactTypeName eq Employee)" |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdByUserID": 1,
      "createdByUserName": "Ava Chen",
      "createdDateTime": "string",
      "modifiedByUserID": {},
      "modifiedByUserName": {},
      "modifiedDateTime": "string",
      "workersCompCode": "string",
      "workersCompID": 1,
      "workersCompName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdByUserID` | number |  |
| `createdByUserName` | string |  |
| `createdDateTime` | string |  |
| `modifiedByUserID` | object |  |
| `modifiedByUserName` | object |  |
| `modifiedDateTime` | string |  |
| `workersCompCode` | string |  |
| `workersCompID` | number |  |
| `workersCompName` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET WorkersComps` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-types.md) for the provider-specific parameters and requirements.

