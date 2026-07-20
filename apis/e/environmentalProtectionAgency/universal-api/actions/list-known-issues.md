# Environmental Protection Agency: List Known Issues

Retrieves known issues from EPA AQS.

```
GET https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-known-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Environmental Protection Agency `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-known-issues?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-known-issues?${params}`, {
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
      "affected_services": "string",
      "description": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affected_services` | string | EPA services affected by the issue. |
| `description` | string | Known issue description. |
| `title` | string | Known issue title. |

## Native endpoint

Through the native Environmental Protection Agency API, this operation is `GET /metaData/issues` (base URL `https://aqs.epa.gov/data/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-known-issues.md) for the provider-specific parameters and requirements.

