# Wistia: Show Customizations

Retrieves customizations for a Wistia media item.

```
GET https://connect.mindcloud.co/v1/universal/wistia/latest/actions/show-customizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wistia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/show-customizations?connectionId=$CONNECTION_ID&mediaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wistia/latest/actions/show-customizations?${params}`, {
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
| `mediaId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoPlay": "string",
      "bpbTime": "string",
      "branding": "string",
      "controlsVisibleOnLoad": "string",
      "copyLinkAndThumbnailEnabled": "https://example.com",
      "doNotTrack": "string",
      "email": "ava@example.com",
      "encrypted": {
        "passwordProtectPassword": "string"
      },
      "endVideoBehavior": "string",
      "fitStrategy": "string",
      "fullscreenButton": "string",
      "fullscreenOnRotateToLandscape": "string",
      "keyMoments": "string",
      "muted": "string",
      "playbackRateControl": "string",
      "playbar": "string",
      "playButton": "string",
      "playerColor": "string",
      "playlistLinks": "https://example.com",
      "playlistLoop": "string",
      "playPauseNotifier": "string",
      "playsinline": "string",
      "playSuspendedOffScreen": "string",
      "plugin": {
        "captionsV1": {
          "on": "string",
          "onByDefault": "string"
        },
        "chapters": {
          "chapterList": [
            {
              "deleted": "string",
              "id": "string",
              "time": "string",
              "title": "string"
            }
          ],
          "on": "string",
          "visibleOnLoad": "string"
        },
        "passwordProtectedVideo": {
          "async": "string",
          "challenge": "string",
          "on": "string",
          "src": "string"
        },
        "postrollV1": {
          "autoSize": "string",
          "conversionOpportunityKey": "string",
          "ctaType": "string",
          "link": "https://example.com",
          "on": "string",
          "rewatch": "string",
          "style": {
            "backgroundColor": "string"
          },
          "text": "string",
          "time": "string"
        },
        "socialbarV1": {
          "buttons": "string",
          "height": "string",
          "showTweetCount": "string",
          "tweetText": "string"
        },
        "videoThumbnail": {
          "clickToPlayButton": "string"
        }
      },
      "preload": "string",
      "private": {
        "passwordProtectOn": "string",
        "showComments": "string"
      },
      "qualityControl": "string",
      "qualityMax": "string",
      "qualityMin": "string",
      "resumable": "string",
      "seo": "string",
      "settingsControl": "string",
      "showCustomerLogo": "string",
      "silentAutoPlay": "string",
      "smallPlayButton": "string",
      "spherical": "string",
      "stillUrl": "https://example.com",
      "thumbnailAltText": "string",
      "time": "string",
      "videoFoam": "string",
      "volume": "string",
      "volumeControl": "string",
      "wmode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoPlay` | string | Whether the video should auto play or not. |
| `bpbTime` | string |  |
| `branding` | string |  |
| `controlsVisibleOnLoad` | string |  |
| `copyLinkAndThumbnailEnabled` | string |  |
| `doNotTrack` | string |  |
| `email` | string |  |
| `encrypted` | object |  |
| `encrypted.passwordProtectPassword` | string |  |
| `endVideoBehavior` | string | Behavior of the video at the end. |
| `fitStrategy` | string |  |
| `fullscreenButton` | string |  |
| `fullscreenOnRotateToLandscape` | string |  |
| `keyMoments` | string | String representation of whether the key moments feature is enabled. |
| `muted` | string |  |
| `playbackRateControl` | string |  |
| `playbar` | string |  |
| `playButton` | string | Indicates if the play button is visible. |
| `playerColor` | string | The color of the video player. |
| `playlistLinks` | string |  |
| `playlistLoop` | string |  |
| `playPauseNotifier` | string |  |
| `playsinline` | string |  |
| `playSuspendedOffScreen` | string |  |
| `plugin` | object |  |
| `plugin.captionsV1` | object | Captions plugin configuration (response format) |
| `plugin.captionsV1.on` | string | String representation of whether the captions plugin is enabled ("true" or "false"). |
| `plugin.captionsV1.onByDefault` | string | String representation of whether captions are turned on by default ("true" or "false"). |
| `plugin.chapters` | object |  |
| `plugin.chapters.chapterList` | array<object> |  |
| `plugin.chapters.chapterList[].deleted` | string |  |
| `plugin.chapters.chapterList[].id` | string |  |
| `plugin.chapters.chapterList[].time` | string |  |
| `plugin.chapters.chapterList[].title` | string |  |
| `plugin.chapters.on` | string |  |
| `plugin.chapters.visibleOnLoad` | string |  |
| `plugin.passwordProtectedVideo` | object |  |
| `plugin.passwordProtectedVideo.async` | string |  |
| `plugin.passwordProtectedVideo.challenge` | string |  |
| `plugin.passwordProtectedVideo.on` | string |  |
| `plugin.passwordProtectedVideo.src` | string |  |
| `plugin.postrollV1` | object | Adds a Call To Action to your Video (response format) |
| `plugin.postrollV1.autoSize` | string | String representation of whether the post-roll will automatically adjust its size. |
| `plugin.postrollV1.conversionOpportunityKey` | string | The key used for tracking conversion opportunities. |
| `plugin.postrollV1.ctaType` | string | The type of call-to-action to be displayed. |
| `plugin.postrollV1.link` | string | The URL of the link to be displayed. |
| `plugin.postrollV1.on` | string | String representation of whether the post-roll is enabled. |
| `plugin.postrollV1.rewatch` | string | String representation of whether the video can be rewatched. |
| `plugin.postrollV1.style` | object |  |
| `plugin.postrollV1.style.backgroundColor` | string | The background color of the post-roll. |
| `plugin.postrollV1.text` | string | The URL of the text to be displayed. |
| `plugin.postrollV1.time` | string | The time when the post-roll should be displayed as a string. |
| `plugin.socialbarV1` | object |  |
| `plugin.socialbarV1.buttons` | string |  |
| `plugin.socialbarV1.height` | string |  |
| `plugin.socialbarV1.showTweetCount` | string |  |
| `plugin.socialbarV1.tweetText` | string |  |
| `plugin.videoThumbnail` | object |  |
| `plugin.videoThumbnail.clickToPlayButton` | string |  |
| `preload` | string |  |
| `private` | object |  |
| `private.passwordProtectOn` | string |  |
| `private.showComments` | string |  |
| `qualityControl` | string |  |
| `qualityMax` | string |  |
| `qualityMin` | string |  |
| `resumable` | string |  |
| `seo` | string |  |
| `settingsControl` | string |  |
| `showCustomerLogo` | string |  |
| `silentAutoPlay` | string |  |
| `smallPlayButton` | string |  |
| `spherical` | string |  |
| `stillUrl` | string |  |
| `thumbnailAltText` | string |  |
| `time` | string |  |
| `videoFoam` | string |  |
| `volume` | string |  |
| `volumeControl` | string |  |
| `wmode` | string |  |

## Native endpoint

Through the native Wistia API, this operation is `GET /modern/medias/:mediaId/customizations` (base URL `https://api.wistia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-customizations.md) for the provider-specific parameters and requirements.

