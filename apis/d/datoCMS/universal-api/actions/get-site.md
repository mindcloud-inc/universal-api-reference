# DatoCMS: Get Site



```
GET https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-site?${params}`, {
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
| `include` | string | no | Comma-separated relationships to include in response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "assetsCdnDefaultSettings": {
          "image": {
            "auto": [
              "string"
            ]
          },
          "video": {
            "disableServingRawVideos": true
          }
        },
        "domain": "string",
        "favicon": "string",
        "forceUseOfSandboxEnvironments": true,
        "globalSeo": "string",
        "googleMapsApiToken": "string",
        "imgixHost": "string",
        "internalDomain": "string",
        "ipTrackingEnabled": true,
        "lastDataChangeAt": "2026-05-07T12:00:00.000Z",
        "locales": [
          "string"
        ],
        "name": "Ava Chen",
        "noIndex": true,
        "require2fa": true,
        "theme": {
          "accentColor": {
            "alpha": 1,
            "blue": 1,
            "green": 1,
            "red": 1
          },
          "darkColor": {
            "alpha": 1,
            "blue": 1,
            "green": 1,
            "red": 1
          },
          "hue": 1,
          "lightColor": {
            "alpha": 1,
            "blue": 1,
            "green": 1,
            "red": 1
          },
          "logo": "string",
          "primaryColor": {
            "alpha": 1,
            "blue": 1,
            "green": 1,
            "red": 1
          },
          "type": "string"
        },
        "timezone": "string"
      },
      "id": "string",
      "meta": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "customUploadStorageSettings": true,
        "draftModeDefault": true,
        "improvedBooleanFields": true,
        "improvedExposureOfInlineBlocksInCda": true,
        "improvedGqlMultilocaleFields": true,
        "improvedGqlVisibilityControl": true,
        "improvedHexManagement": true,
        "improvedItemsListing": true,
        "improvedTimezoneManagement": true,
        "improvedValidationAtPublishing": true,
        "millisecondsInDatetime": true
      },
      "relationships": {
        "account": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "itemTypes": {
          "data": [
            {
              "id": "string",
              "type": "string"
            }
          ]
        },
        "owner": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.assetsCdnDefaultSettings.image.auto` | array<string> |  |
| `attributes.assetsCdnDefaultSettings.video.disableServingRawVideos` | boolean |  |
| `attributes.domain` | string |  |
| `attributes.favicon` | string |  |
| `attributes.forceUseOfSandboxEnvironments` | boolean |  |
| `attributes.globalSeo` | string |  |
| `attributes.googleMapsApiToken` | string |  |
| `attributes.imgixHost` | string |  |
| `attributes.internalDomain` | string |  |
| `attributes.ipTrackingEnabled` | boolean |  |
| `attributes.lastDataChangeAt` | date |  |
| `attributes.locales` | array<string> |  |
| `attributes.name` | string |  |
| `attributes.noIndex` | boolean |  |
| `attributes.require2fa` | boolean |  |
| `attributes.theme.accentColor.alpha` | number |  |
| `attributes.theme.accentColor.blue` | number |  |
| `attributes.theme.accentColor.green` | number |  |
| `attributes.theme.accentColor.red` | number |  |
| `attributes.theme.darkColor.alpha` | number |  |
| `attributes.theme.darkColor.blue` | number |  |
| `attributes.theme.darkColor.green` | number |  |
| `attributes.theme.darkColor.red` | number |  |
| `attributes.theme.hue` | number |  |
| `attributes.theme.lightColor.alpha` | number |  |
| `attributes.theme.lightColor.blue` | number |  |
| `attributes.theme.lightColor.green` | number |  |
| `attributes.theme.lightColor.red` | number |  |
| `attributes.theme.logo` | string |  |
| `attributes.theme.primaryColor.alpha` | number |  |
| `attributes.theme.primaryColor.blue` | number |  |
| `attributes.theme.primaryColor.green` | number |  |
| `attributes.theme.primaryColor.red` | number |  |
| `attributes.theme.type` | string |  |
| `attributes.timezone` | string |  |
| `id` | string |  |
| `meta.createdAt` | date |  |
| `meta.customUploadStorageSettings` | boolean |  |
| `meta.draftModeDefault` | boolean |  |
| `meta.improvedBooleanFields` | boolean |  |
| `meta.improvedExposureOfInlineBlocksInCda` | boolean |  |
| `meta.improvedGqlMultilocaleFields` | boolean |  |
| `meta.improvedGqlVisibilityControl` | boolean |  |
| `meta.improvedHexManagement` | boolean |  |
| `meta.improvedItemsListing` | boolean |  |
| `meta.improvedTimezoneManagement` | boolean |  |
| `meta.improvedValidationAtPublishing` | boolean |  |
| `meta.millisecondsInDatetime` | boolean |  |
| `relationships.account.data.id` | string |  |
| `relationships.account.data.type` | string |  |
| `relationships.itemTypes.data[].id` | string |  |
| `relationships.itemTypes.data[].type` | string |  |
| `relationships.owner.data.id` | string |  |
| `relationships.owner.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `GET /site` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

