# UpGuard: Start Monitoring Vendor

Starts monitoring a vendor in UpGuard.

```
POST https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/start-monitoring-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/start-monitoring-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/start-monitoring-vendor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vendorId` | number | no | The numeric ID of the vendor to begin monitoring. |
| `hostname` | string | no | The hostname of the vendor to begin monitoring when no vendor ID is provided. |
| `labels[]` | array<string> | no | Labels to assign to the vendor when monitoring starts. Accepts multiple values in one string, delimited by `,`. |
| `tier` | number | no | Tier to assign to the vendor. |
| `waitForScan` | boolean | no | Wait for scan results on new unknown vendors before returning. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assessmentStatus": "string",
      "automatedScore": 1,
      "categoryRiskCounts": {
        "attackSurface": {
          "critical": 1,
          "high": 1,
          "low": 1,
          "medium": 1
        },
        "brandProtection": {
          "critical": 1,
          "high": 1,
          "low": 1,
          "medium": 1
        },
        "brandReputation": {
          "critical": 1,
          "high": 1,
          "low": 1,
          "medium": 1
        },
        "dataLeakage": {
          "critical": 1,
          "high": 1,
          "low": 1,
          "medium": 1
        },
        "dns": {
          "critical": 1,
          "high": 1,
          "low": 1,
          "medium": 1
        },
        "emailSecurity": {
          "critical": 1,
          "high": 1,
          "low": 1,
          "medium": 1
        },
        "encryption": {
          "critical": 1,
          "high": 1,
          "low": 1,
          "medium": 1
        },
        "ipDomainReputation": {
          "critical": 1,
          "high": 1,
          "low": 1,
          "medium": 1
        },
        "networkSecurity": {
          "critical": 1,
          "high": 1,
          "low": 1,
          "medium": 1
        },
        "operationalRisk": {
          "critical": 1,
          "high": 1,
          "low": 1,
          "medium": 1
        },
        "phishing": {
          "critical": 1,
          "high": 1,
          "low": 1,
          "medium": 1
        },
        "questionnaires": {
          "critical": 1,
          "high": 1,
          "low": 1,
          "medium": 1
        },
        "vulnerabilityManagement": {
          "critical": 1,
          "high": 1,
          "low": 1,
          "medium": 1
        },
        "websiteSecurity": {
          "critical": 1,
          "high": 1,
          "low": 1,
          "medium": 1
        }
      },
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
      "domainCountActive": 1,
      "domainCountInactive": 1,
      "domainCountTotal": 1,
      "firstMonitored": "string",
      "id": 1,
      "industryAverageScore": 1,
      "industryGroup": "string",
      "industrySector": "string",
      "name": "Ava Chen",
      "note": {},
      "overallRiskCounts": {
        "critical": 1,
        "high": 1,
        "low": 1,
        "medium": 1
      },
      "overallScore": 1,
      "portfolios": [
        "string"
      ],
      "primaryHostname": "Ava Chen",
      "score": 1,
      "scoresByEpoch": [
        {
          "attackSurface": 1,
          "brandReputation": 1,
          "dataLeakage": 1,
          "dns": 1,
          "emailSecurity": 1,
          "encryption": 1,
          "epoch": "string",
          "ipDomainReputation": 1,
          "networkSecurity": 1,
          "operationalRisk": 1,
          "overall": 1,
          "vulnerabilityManagement": 1,
          "websiteSecurity": 1,
          "when": "string"
        }
      ],
      "vendorMetadata": {
        "employeeCount": 1,
        "legalName": "Ava Chen",
        "locationCity": "string",
        "locationCountry": "string",
        "locationPostcode": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assessmentStatus` | string |  |
| `automatedScore` | number |  |
| `categoryRiskCounts.attackSurface.critical` | number |  |
| `categoryRiskCounts.attackSurface.high` | number |  |
| `categoryRiskCounts.attackSurface.low` | number |  |
| `categoryRiskCounts.attackSurface.medium` | number |  |
| `categoryRiskCounts.brandProtection.critical` | number |  |
| `categoryRiskCounts.brandProtection.high` | number |  |
| `categoryRiskCounts.brandProtection.low` | number |  |
| `categoryRiskCounts.brandProtection.medium` | number |  |
| `categoryRiskCounts.brandReputation.critical` | number |  |
| `categoryRiskCounts.brandReputation.high` | number |  |
| `categoryRiskCounts.brandReputation.low` | number |  |
| `categoryRiskCounts.brandReputation.medium` | number |  |
| `categoryRiskCounts.dataLeakage.critical` | number |  |
| `categoryRiskCounts.dataLeakage.high` | number |  |
| `categoryRiskCounts.dataLeakage.low` | number |  |
| `categoryRiskCounts.dataLeakage.medium` | number |  |
| `categoryRiskCounts.dns.critical` | number |  |
| `categoryRiskCounts.dns.high` | number |  |
| `categoryRiskCounts.dns.low` | number |  |
| `categoryRiskCounts.dns.medium` | number |  |
| `categoryRiskCounts.emailSecurity.critical` | number |  |
| `categoryRiskCounts.emailSecurity.high` | number |  |
| `categoryRiskCounts.emailSecurity.low` | number |  |
| `categoryRiskCounts.emailSecurity.medium` | number |  |
| `categoryRiskCounts.encryption.critical` | number |  |
| `categoryRiskCounts.encryption.high` | number |  |
| `categoryRiskCounts.encryption.low` | number |  |
| `categoryRiskCounts.encryption.medium` | number |  |
| `categoryRiskCounts.ipDomainReputation.critical` | number |  |
| `categoryRiskCounts.ipDomainReputation.high` | number |  |
| `categoryRiskCounts.ipDomainReputation.low` | number |  |
| `categoryRiskCounts.ipDomainReputation.medium` | number |  |
| `categoryRiskCounts.networkSecurity.critical` | number |  |
| `categoryRiskCounts.networkSecurity.high` | number |  |
| `categoryRiskCounts.networkSecurity.low` | number |  |
| `categoryRiskCounts.networkSecurity.medium` | number |  |
| `categoryRiskCounts.operationalRisk.critical` | number |  |
| `categoryRiskCounts.operationalRisk.high` | number |  |
| `categoryRiskCounts.operationalRisk.low` | number |  |
| `categoryRiskCounts.operationalRisk.medium` | number |  |
| `categoryRiskCounts.phishing.critical` | number |  |
| `categoryRiskCounts.phishing.high` | number |  |
| `categoryRiskCounts.phishing.low` | number |  |
| `categoryRiskCounts.phishing.medium` | number |  |
| `categoryRiskCounts.questionnaires.critical` | number |  |
| `categoryRiskCounts.questionnaires.high` | number |  |
| `categoryRiskCounts.questionnaires.low` | number |  |
| `categoryRiskCounts.questionnaires.medium` | number |  |
| `categoryRiskCounts.vulnerabilityManagement.critical` | number |  |
| `categoryRiskCounts.vulnerabilityManagement.high` | number |  |
| `categoryRiskCounts.vulnerabilityManagement.low` | number |  |
| `categoryRiskCounts.vulnerabilityManagement.medium` | number |  |
| `categoryRiskCounts.websiteSecurity.critical` | number |  |
| `categoryRiskCounts.websiteSecurity.high` | number |  |
| `categoryRiskCounts.websiteSecurity.low` | number |  |
| `categoryRiskCounts.websiteSecurity.medium` | number |  |
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
| `domainCountActive` | number |  |
| `domainCountInactive` | number |  |
| `domainCountTotal` | number |  |
| `firstMonitored` | string |  |
| `id` | number |  |
| `industryAverageScore` | number |  |
| `industryGroup` | string |  |
| `industrySector` | string |  |
| `name` | string |  |
| `note` | object |  |
| `overallRiskCounts.critical` | number |  |
| `overallRiskCounts.high` | number |  |
| `overallRiskCounts.low` | number |  |
| `overallRiskCounts.medium` | number |  |
| `overallScore` | number |  |
| `portfolios[]` | string |  |
| `primaryHostname` | string |  |
| `score` | number |  |
| `scoresByEpoch[].attackSurface` | number |  |
| `scoresByEpoch[].brandReputation` | number |  |
| `scoresByEpoch[].dataLeakage` | number |  |
| `scoresByEpoch[].dns` | number |  |
| `scoresByEpoch[].emailSecurity` | number |  |
| `scoresByEpoch[].encryption` | number |  |
| `scoresByEpoch[].epoch` | string |  |
| `scoresByEpoch[].ipDomainReputation` | number |  |
| `scoresByEpoch[].networkSecurity` | number |  |
| `scoresByEpoch[].operationalRisk` | number |  |
| `scoresByEpoch[].overall` | number |  |
| `scoresByEpoch[].vulnerabilityManagement` | number |  |
| `scoresByEpoch[].websiteSecurity` | number |  |
| `scoresByEpoch[].when` | string |  |
| `vendorMetadata.employeeCount` | number |  |
| `vendorMetadata.legalName` | string |  |
| `vendorMetadata.locationCity` | string |  |
| `vendorMetadata.locationCountry` | string |  |
| `vendorMetadata.locationPostcode` | string |  |

## Native endpoint

Through the native UpGuard API, this operation is `POST /vendor/monitor` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-monitoring-vendor.md) for the provider-specific parameters and requirements.

