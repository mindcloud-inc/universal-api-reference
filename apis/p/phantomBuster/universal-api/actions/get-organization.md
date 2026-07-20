# PhantomBuster: Get Organization

Retrieves organization details from PhantomBuster.

```
GET https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-organization?${params}`, {
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
| `withCrmIntegrations` | string | no |  |
| `withCustomPrompts` | string | no |  |
| `withGlobalObject` | string | no |  |
| `withProxies` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingFirstName": "Ava",
      "billingLastName": "Chen",
      "billingMail": "string",
      "company": "string",
      "createdAt": 1,
      "dailyAiCredit": 1,
      "dailyCaptcha": 1,
      "dailyDiscoveredMail": 1,
      "dailyExecutionTime": 1,
      "dailyMail": 1,
      "displayName": "Ava Chen",
      "id": "string",
      "isV3": true,
      "name": "Ava Chen",
      "plan": {
        "agents": 1,
        "isAvailable": true,
        "name": "Ava Chen",
        "parallelism": 1,
        "scripts": 1
      },
      "planSlug": "string",
      "planStartedAt": 1,
      "s3Folder": "string",
      "s3Storage": 1,
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingFirstName` | string |  |
| `billingLastName` | string |  |
| `billingMail` | string |  |
| `company` | string |  |
| `createdAt` | number |  |
| `dailyAiCredit` | number |  |
| `dailyCaptcha` | number |  |
| `dailyDiscoveredMail` | number |  |
| `dailyExecutionTime` | number |  |
| `dailyMail` | number |  |
| `displayName` | string |  |
| `id` | string |  |
| `isV3` | boolean |  |
| `name` | string |  |
| `plan.agents` | number |  |
| `plan.isAvailable` | boolean |  |
| `plan.name` | string |  |
| `plan.parallelism` | number |  |
| `plan.scripts` | number |  |
| `planSlug` | string |  |
| `planStartedAt` | number |  |
| `s3Folder` | string |  |
| `s3Storage` | number |  |
| `timezone` | string |  |

## Native endpoint

Through the native PhantomBuster API, this operation is `GET /orgs/fetch` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

