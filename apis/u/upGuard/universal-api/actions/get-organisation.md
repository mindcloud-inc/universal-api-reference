# UpGuard: Get Organisation

Retrieves your organisation details from UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-organisation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-organisation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-organisation?${params}`, {
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
      "automatedScore": 1,
      "categoryScores": {
        "attackSurface": 1,
        "brandReputation": 1,
        "dataLeakage": 1,
        "dns": 1,
        "emailSecurity": 1,
        "encryption": 1,
        "ipDomainReputation": 1,
        "networkSecurity": 1,
        "operationalRisk": 1,
        "vulnerabilityManagement": 1,
        "websiteSecurity": 1
      },
      "id": 1,
      "name": "Ava Chen",
      "primaryHostname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automatedScore` | number |  |
| `categoryScores.attackSurface` | number |  |
| `categoryScores.brandReputation` | number |  |
| `categoryScores.dataLeakage` | number |  |
| `categoryScores.dns` | number |  |
| `categoryScores.emailSecurity` | number |  |
| `categoryScores.encryption` | number |  |
| `categoryScores.ipDomainReputation` | number |  |
| `categoryScores.networkSecurity` | number |  |
| `categoryScores.operationalRisk` | number |  |
| `categoryScores.vulnerabilityManagement` | number |  |
| `categoryScores.websiteSecurity` | number |  |
| `id` | number |  |
| `name` | string |  |
| `primaryHostname` | string |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /organisation` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organisation.md) for the provider-specific parameters and requirements.

