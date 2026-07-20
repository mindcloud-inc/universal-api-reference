# Cloudmersive Security: Detect SQL Injection

Detects SQL injection threats in Cloudmersive Security.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-sql-injection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Security `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-sql-injection?connectionId=$CONNECTION_ID&inputText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputText": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-sql-injection?${params}`, {
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
| `inputText` | string | yes | Text input to scan for SQL injection attacks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ContainedSqlInjectionAttack": true,
      "OriginalInput": "string",
      "Successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ContainedSqlInjectionAttack` | boolean |  |
| `OriginalInput` | string |  |
| `Successful` | boolean |  |

## Native endpoint

Through the native Cloudmersive Security API, this operation is `POST /security/threat-detection/content/sql-injection/detect/string` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-sql-injection.md) for the provider-specific parameters and requirements.

