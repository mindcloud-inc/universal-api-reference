# Brevo: Get Email Campaign



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-email-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-email-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-email-campaign?${params}`, {
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
| `campaignId` | string | yes | Email campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abTesting": true,
      "createdAt": "string",
      "footer": "string",
      "header": "string",
      "htmlContent": "string",
      "id": 1,
      "inlineImageActivation": true,
      "mirrorActive": true,
      "modifiedAt": "string",
      "name": "Ava Chen",
      "previewText": "string",
      "recipients": {
        "lists": [
          1
        ]
      },
      "replyTo": "string",
      "scheduledAt": "string",
      "sendAtBestTime": true,
      "sender": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      },
      "shareLink": "https://example.com",
      "statistics": {
        "globalStats": {
          "appleMppOpens": 1,
          "clickers": 1,
          "complaints": 1,
          "delivered": 1,
          "estimatedViews": 1,
          "hardBounces": 1,
          "opensRate": 1,
          "sent": 1,
          "softBounces": 1,
          "trackableViews": 1,
          "trackableViewsRate": 1,
          "uniqueClicks": 1,
          "uniqueViews": 1,
          "unsubscriptions": 1,
          "viewed": 1
        },
        "mirrorClick": 1,
        "remaining": 1,
        "statsByBrowser": {
          "android": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          },
          "chrome": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          },
          "edge": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          },
          "electron": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          },
          "firefox": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          },
          "internetexplorer": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          },
          "mailchannelsscanner": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          },
          "microsoft": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          },
          "mozilla": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          },
          "opera": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          },
          "outlookexpress": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          },
          "safari": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          },
          "thunderbird": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          },
          "unknown": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          },
          "yahoomailproxy": {
            "clickers": 1,
            "trackableViews": 1,
            "uniqueClicks": 1,
            "uniqueViews": 1,
            "viewed": 1
          }
        },
        "statsByDevice": {
          "desktop": {
            "mac": {
              "clickers": 1,
              "trackableViews": 1,
              "uniqueClicks": 1,
              "uniqueViews": 1,
              "viewed": 1
            },
            "othersystem": {
              "clickers": 1,
              "trackableViews": 1,
              "uniqueClicks": 1,
              "uniqueViews": 1,
              "viewed": 1
            },
            "windows": {
              "clickers": 1,
              "trackableViews": 1,
              "uniqueClicks": 1,
              "uniqueViews": 1,
              "viewed": 1
            }
          },
          "mobile": {
            "androidmobile": {
              "clickers": 1,
              "trackableViews": 1,
              "uniqueClicks": 1,
              "uniqueViews": 1,
              "viewed": 1
            },
            "iphone": {
              "clickers": 1,
              "trackableViews": 1,
              "uniqueClicks": 1,
              "uniqueViews": 1,
              "viewed": 1
            }
          },
          "tablet": {
            "androidtablet": {
              "clickers": 1,
              "trackableViews": 1,
              "uniqueClicks": 1,
              "uniqueViews": 1,
              "viewed": 1
            },
            "appleipad": {
              "clickers": 1,
              "trackableViews": 1,
              "uniqueClicks": 1,
              "uniqueViews": 1,
              "viewed": 1
            }
          }
        }
      },
      "status": "string",
      "subject": "string",
      "tag": "string",
      "testSent": true,
      "toField": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abTesting` | boolean |  |
| `createdAt` | string |  |
| `footer` | string |  |
| `header` | string |  |
| `htmlContent` | string |  |
| `id` | number |  |
| `inlineImageActivation` | boolean |  |
| `mirrorActive` | boolean |  |
| `modifiedAt` | string |  |
| `name` | string |  |
| `previewText` | string |  |
| `recipients.lists[]` | number |  |
| `replyTo` | string |  |
| `scheduledAt` | string |  |
| `sendAtBestTime` | boolean |  |
| `sender.email` | string |  |
| `sender.id` | number |  |
| `sender.name` | string |  |
| `shareLink` | string |  |
| `statistics.globalStats.appleMppOpens` | number |  |
| `statistics.globalStats.clickers` | number |  |
| `statistics.globalStats.complaints` | number |  |
| `statistics.globalStats.delivered` | number |  |
| `statistics.globalStats.estimatedViews` | number |  |
| `statistics.globalStats.hardBounces` | number |  |
| `statistics.globalStats.opensRate` | number |  |
| `statistics.globalStats.sent` | number |  |
| `statistics.globalStats.softBounces` | number |  |
| `statistics.globalStats.trackableViews` | number |  |
| `statistics.globalStats.trackableViewsRate` | number |  |
| `statistics.globalStats.uniqueClicks` | number |  |
| `statistics.globalStats.uniqueViews` | number |  |
| `statistics.globalStats.unsubscriptions` | number |  |
| `statistics.globalStats.viewed` | number |  |
| `statistics.mirrorClick` | number |  |
| `statistics.remaining` | number |  |
| `statistics.statsByBrowser.android.clickers` | number |  |
| `statistics.statsByBrowser.android.trackableViews` | number |  |
| `statistics.statsByBrowser.android.uniqueClicks` | number |  |
| `statistics.statsByBrowser.android.uniqueViews` | number |  |
| `statistics.statsByBrowser.android.viewed` | number |  |
| `statistics.statsByBrowser.chrome.clickers` | number |  |
| `statistics.statsByBrowser.chrome.trackableViews` | number |  |
| `statistics.statsByBrowser.chrome.uniqueClicks` | number |  |
| `statistics.statsByBrowser.chrome.uniqueViews` | number |  |
| `statistics.statsByBrowser.chrome.viewed` | number |  |
| `statistics.statsByBrowser.edge.clickers` | number |  |
| `statistics.statsByBrowser.edge.trackableViews` | number |  |
| `statistics.statsByBrowser.edge.uniqueClicks` | number |  |
| `statistics.statsByBrowser.edge.uniqueViews` | number |  |
| `statistics.statsByBrowser.edge.viewed` | number |  |
| `statistics.statsByBrowser.electron.clickers` | number |  |
| `statistics.statsByBrowser.electron.trackableViews` | number |  |
| `statistics.statsByBrowser.electron.uniqueClicks` | number |  |
| `statistics.statsByBrowser.electron.uniqueViews` | number |  |
| `statistics.statsByBrowser.electron.viewed` | number |  |
| `statistics.statsByBrowser.firefox.clickers` | number |  |
| `statistics.statsByBrowser.firefox.trackableViews` | number |  |
| `statistics.statsByBrowser.firefox.uniqueClicks` | number |  |
| `statistics.statsByBrowser.firefox.uniqueViews` | number |  |
| `statistics.statsByBrowser.firefox.viewed` | number |  |
| `statistics.statsByBrowser.internetexplorer.clickers` | number |  |
| `statistics.statsByBrowser.internetexplorer.trackableViews` | number |  |
| `statistics.statsByBrowser.internetexplorer.uniqueClicks` | number |  |
| `statistics.statsByBrowser.internetexplorer.uniqueViews` | number |  |
| `statistics.statsByBrowser.internetexplorer.viewed` | number |  |
| `statistics.statsByBrowser.mailchannelsscanner.clickers` | number |  |
| `statistics.statsByBrowser.mailchannelsscanner.trackableViews` | number |  |
| `statistics.statsByBrowser.mailchannelsscanner.uniqueClicks` | number |  |
| `statistics.statsByBrowser.mailchannelsscanner.uniqueViews` | number |  |
| `statistics.statsByBrowser.mailchannelsscanner.viewed` | number |  |
| `statistics.statsByBrowser.microsoft.clickers` | number |  |
| `statistics.statsByBrowser.microsoft.trackableViews` | number |  |
| `statistics.statsByBrowser.microsoft.uniqueClicks` | number |  |
| `statistics.statsByBrowser.microsoft.uniqueViews` | number |  |
| `statistics.statsByBrowser.microsoft.viewed` | number |  |
| `statistics.statsByBrowser.mozilla.clickers` | number |  |
| `statistics.statsByBrowser.mozilla.trackableViews` | number |  |
| `statistics.statsByBrowser.mozilla.uniqueClicks` | number |  |
| `statistics.statsByBrowser.mozilla.uniqueViews` | number |  |
| `statistics.statsByBrowser.mozilla.viewed` | number |  |
| `statistics.statsByBrowser.opera.clickers` | number |  |
| `statistics.statsByBrowser.opera.trackableViews` | number |  |
| `statistics.statsByBrowser.opera.uniqueClicks` | number |  |
| `statistics.statsByBrowser.opera.uniqueViews` | number |  |
| `statistics.statsByBrowser.opera.viewed` | number |  |
| `statistics.statsByBrowser.outlookexpress.clickers` | number |  |
| `statistics.statsByBrowser.outlookexpress.trackableViews` | number |  |
| `statistics.statsByBrowser.outlookexpress.uniqueClicks` | number |  |
| `statistics.statsByBrowser.outlookexpress.uniqueViews` | number |  |
| `statistics.statsByBrowser.outlookexpress.viewed` | number |  |
| `statistics.statsByBrowser.safari.clickers` | number |  |
| `statistics.statsByBrowser.safari.trackableViews` | number |  |
| `statistics.statsByBrowser.safari.uniqueClicks` | number |  |
| `statistics.statsByBrowser.safari.uniqueViews` | number |  |
| `statistics.statsByBrowser.safari.viewed` | number |  |
| `statistics.statsByBrowser.thunderbird.clickers` | number |  |
| `statistics.statsByBrowser.thunderbird.trackableViews` | number |  |
| `statistics.statsByBrowser.thunderbird.uniqueClicks` | number |  |
| `statistics.statsByBrowser.thunderbird.uniqueViews` | number |  |
| `statistics.statsByBrowser.thunderbird.viewed` | number |  |
| `statistics.statsByBrowser.unknown.clickers` | number |  |
| `statistics.statsByBrowser.unknown.trackableViews` | number |  |
| `statistics.statsByBrowser.unknown.uniqueClicks` | number |  |
| `statistics.statsByBrowser.unknown.uniqueViews` | number |  |
| `statistics.statsByBrowser.unknown.viewed` | number |  |
| `statistics.statsByBrowser.yahoomailproxy.clickers` | number |  |
| `statistics.statsByBrowser.yahoomailproxy.trackableViews` | number |  |
| `statistics.statsByBrowser.yahoomailproxy.uniqueClicks` | number |  |
| `statistics.statsByBrowser.yahoomailproxy.uniqueViews` | number |  |
| `statistics.statsByBrowser.yahoomailproxy.viewed` | number |  |
| `statistics.statsByDevice.desktop.mac.clickers` | number |  |
| `statistics.statsByDevice.desktop.mac.trackableViews` | number |  |
| `statistics.statsByDevice.desktop.mac.uniqueClicks` | number |  |
| `statistics.statsByDevice.desktop.mac.uniqueViews` | number |  |
| `statistics.statsByDevice.desktop.mac.viewed` | number |  |
| `statistics.statsByDevice.desktop.othersystem.clickers` | number |  |
| `statistics.statsByDevice.desktop.othersystem.trackableViews` | number |  |
| `statistics.statsByDevice.desktop.othersystem.uniqueClicks` | number |  |
| `statistics.statsByDevice.desktop.othersystem.uniqueViews` | number |  |
| `statistics.statsByDevice.desktop.othersystem.viewed` | number |  |
| `statistics.statsByDevice.desktop.windows.clickers` | number |  |
| `statistics.statsByDevice.desktop.windows.trackableViews` | number |  |
| `statistics.statsByDevice.desktop.windows.uniqueClicks` | number |  |
| `statistics.statsByDevice.desktop.windows.uniqueViews` | number |  |
| `statistics.statsByDevice.desktop.windows.viewed` | number |  |
| `statistics.statsByDevice.mobile.androidmobile.clickers` | number |  |
| `statistics.statsByDevice.mobile.androidmobile.trackableViews` | number |  |
| `statistics.statsByDevice.mobile.androidmobile.uniqueClicks` | number |  |
| `statistics.statsByDevice.mobile.androidmobile.uniqueViews` | number |  |
| `statistics.statsByDevice.mobile.androidmobile.viewed` | number |  |
| `statistics.statsByDevice.mobile.iphone.clickers` | number |  |
| `statistics.statsByDevice.mobile.iphone.trackableViews` | number |  |
| `statistics.statsByDevice.mobile.iphone.uniqueClicks` | number |  |
| `statistics.statsByDevice.mobile.iphone.uniqueViews` | number |  |
| `statistics.statsByDevice.mobile.iphone.viewed` | number |  |
| `statistics.statsByDevice.tablet.androidtablet.clickers` | number |  |
| `statistics.statsByDevice.tablet.androidtablet.trackableViews` | number |  |
| `statistics.statsByDevice.tablet.androidtablet.uniqueClicks` | number |  |
| `statistics.statsByDevice.tablet.androidtablet.uniqueViews` | number |  |
| `statistics.statsByDevice.tablet.androidtablet.viewed` | number |  |
| `statistics.statsByDevice.tablet.appleipad.clickers` | number |  |
| `statistics.statsByDevice.tablet.appleipad.trackableViews` | number |  |
| `statistics.statsByDevice.tablet.appleipad.uniqueClicks` | number |  |
| `statistics.statsByDevice.tablet.appleipad.uniqueViews` | number |  |
| `statistics.statsByDevice.tablet.appleipad.viewed` | number |  |
| `status` | string |  |
| `subject` | string |  |
| `tag` | string |  |
| `testSent` | boolean |  |
| `toField` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/emailCampaigns/:campaignId` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-campaign.md) for the provider-specific parameters and requirements.

