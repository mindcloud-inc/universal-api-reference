# Instasent: Get Project Info



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-project-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-project-info?connectionId=$CONNECTION_ID&project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-project-info?${params}`, {
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
| `project` | string | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entity": {
        "attributionConfig": {
          "hoursCampaignCta": 1,
          "hoursCampaignHighIntent": 1,
          "hoursCampaignOpen": 1,
          "hoursCampaignReply": 1,
          "hoursFindOutboundSms": 1,
          "hoursOtherCampaignSent": 1,
          "hoursRcsCampaignSent": 1,
          "hoursSmsCampaignSent": 1,
          "hoursWhatsappCampaignSent": 1
        },
        "brand": {},
        "businessContactsSize": {},
        "businessType": "string",
        "businessUrl": {},
        "conversionConfig": {},
        "createdAt": "string",
        "defaultSmsSender": {},
        "description": "string",
        "generalConfig": {
          "channelDefaults": {
            "autoCreateContactsOnInbounds": true,
            "autoCreateContactsOnOutbounds": true,
            "autoMarketingOptInOnInbound": true,
            "defaultSendingPurpose": {},
            "marketingOptInScope": "string",
            "marketingOptOutScope": "string",
            "optInKeywords": [
              "string"
            ],
            "optOutKeywords": [
              "string"
            ]
          },
          "channelEmail": {
            "autoCreateContactsOnInbounds": {},
            "autoCreateContactsOnOutbounds": {},
            "autoMarketingOptInOnInbound": {},
            "defaultSendingPurpose": {},
            "marketingOptInScope": {},
            "marketingOptOutScope": {},
            "optInKeywords": {},
            "optOutKeywords": {}
          },
          "channelSms": {
            "autoCreateContactsOnInbounds": {},
            "autoCreateContactsOnOutbounds": {},
            "autoMarketingOptInOnInbound": {},
            "defaultSendingPurpose": {},
            "marketingOptInScope": {},
            "marketingOptOutScope": {},
            "optInKeywords": {},
            "optOutKeywords": {}
          }
        },
        "id": "string",
        "locale": "string",
        "lockedReason": {},
        "lockedUntil": {},
        "name": "Ava Chen",
        "projectStatus": "string",
        "projectType": "string",
        "shortTrackingDomain": {},
        "timezone": "string",
        "uid": "string",
        "unsubscribeTrackingDomain": {},
        "updatedAt": "string"
      },
      "metadata": {
        "organization": {
          "account": {
            "credit": {
              "currency": "string",
              "resetAt": {},
              "resetTo": 1,
              "value": 1
            },
            "funds": {
              "currency": "string",
              "value": 1
            }
          },
          "api": {
            "tier": 1
          },
          "id": "string",
          "name": "Ava Chen",
          "plan": {
            "key": "string",
            "quality": 1,
            "status": "string"
          }
        },
        "scopes": [
          "string"
        ],
        "uniqueAttributes": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity.attributionConfig.hoursCampaignCta` | number |  |
| `entity.attributionConfig.hoursCampaignHighIntent` | number |  |
| `entity.attributionConfig.hoursCampaignOpen` | number |  |
| `entity.attributionConfig.hoursCampaignReply` | number |  |
| `entity.attributionConfig.hoursFindOutboundSms` | number |  |
| `entity.attributionConfig.hoursOtherCampaignSent` | number |  |
| `entity.attributionConfig.hoursRcsCampaignSent` | number |  |
| `entity.attributionConfig.hoursSmsCampaignSent` | number |  |
| `entity.attributionConfig.hoursWhatsappCampaignSent` | number |  |
| `entity.brand` | object |  |
| `entity.businessContactsSize` | object |  |
| `entity.businessType` | string |  |
| `entity.businessUrl` | object |  |
| `entity.conversionConfig` | object |  |
| `entity.createdAt` | string |  |
| `entity.defaultSmsSender` | object |  |
| `entity.description` | string |  |
| `entity.generalConfig.channelDefaults.autoCreateContactsOnInbounds` | boolean |  |
| `entity.generalConfig.channelDefaults.autoCreateContactsOnOutbounds` | boolean |  |
| `entity.generalConfig.channelDefaults.autoMarketingOptInOnInbound` | boolean |  |
| `entity.generalConfig.channelDefaults.defaultSendingPurpose` | object |  |
| `entity.generalConfig.channelDefaults.marketingOptInScope` | string |  |
| `entity.generalConfig.channelDefaults.marketingOptOutScope` | string |  |
| `entity.generalConfig.channelDefaults.optInKeywords[]` | string |  |
| `entity.generalConfig.channelDefaults.optOutKeywords[]` | string |  |
| `entity.generalConfig.channelEmail.autoCreateContactsOnInbounds` | object |  |
| `entity.generalConfig.channelEmail.autoCreateContactsOnOutbounds` | object |  |
| `entity.generalConfig.channelEmail.autoMarketingOptInOnInbound` | object |  |
| `entity.generalConfig.channelEmail.defaultSendingPurpose` | object |  |
| `entity.generalConfig.channelEmail.marketingOptInScope` | object |  |
| `entity.generalConfig.channelEmail.marketingOptOutScope` | object |  |
| `entity.generalConfig.channelEmail.optInKeywords` | object |  |
| `entity.generalConfig.channelEmail.optOutKeywords` | object |  |
| `entity.generalConfig.channelSms.autoCreateContactsOnInbounds` | object |  |
| `entity.generalConfig.channelSms.autoCreateContactsOnOutbounds` | object |  |
| `entity.generalConfig.channelSms.autoMarketingOptInOnInbound` | object |  |
| `entity.generalConfig.channelSms.defaultSendingPurpose` | object |  |
| `entity.generalConfig.channelSms.marketingOptInScope` | object |  |
| `entity.generalConfig.channelSms.marketingOptOutScope` | object |  |
| `entity.generalConfig.channelSms.optInKeywords` | object |  |
| `entity.generalConfig.channelSms.optOutKeywords` | object |  |
| `entity.id` | string |  |
| `entity.locale` | string |  |
| `entity.lockedReason` | object |  |
| `entity.lockedUntil` | object |  |
| `entity.name` | string |  |
| `entity.projectStatus` | string |  |
| `entity.projectType` | string |  |
| `entity.shortTrackingDomain` | object |  |
| `entity.timezone` | string |  |
| `entity.uid` | string |  |
| `entity.unsubscribeTrackingDomain` | object |  |
| `entity.updatedAt` | string |  |
| `metadata.organization.account.credit.currency` | string |  |
| `metadata.organization.account.credit.resetAt` | object |  |
| `metadata.organization.account.credit.resetTo` | number |  |
| `metadata.organization.account.credit.value` | number |  |
| `metadata.organization.account.funds.currency` | string |  |
| `metadata.organization.account.funds.value` | number |  |
| `metadata.organization.api.tier` | number |  |
| `metadata.organization.id` | string |  |
| `metadata.organization.name` | string |  |
| `metadata.organization.plan.key` | string |  |
| `metadata.organization.plan.quality` | number |  |
| `metadata.organization.plan.status` | string |  |
| `metadata.scopes[]` | string |  |
| `metadata.uniqueAttributes[]` | string |  |

## Native endpoint

Through the native Instasent API, this operation is `GET /project/:project` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-info.md) for the provider-specific parameters and requirements.

