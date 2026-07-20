# Gamalogic: Verify Email



```
GET https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gamalogic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/verify-email?connectionId=$CONNECTION_ID&emailId=person%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailId": "person@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/verify-email?${params}`, {
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
| `emailId` | string | yes | Email address to validate. Example: `person@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `speedRank` | number | no | Optional speed and accuracy setting. Defaults to 0; higher values are slower and more accurate. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gamalogicEmailidVrfy": [
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
| `gamalogicEmailidVrfy` | array<object> | Email verification result rows returned by Gamalogic. |

## Native endpoint

Through the native Gamalogic API, this operation is `GET /emailvrf` (base URL `https://gamalogic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

