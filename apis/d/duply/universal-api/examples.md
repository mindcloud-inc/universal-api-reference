# Duply Universal API Examples

These examples use the MindCloud API key and Duply connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Usage

Retrieves your current usage from Duply.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/duply/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/duply/latest/actions/get-usage?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "cycleImageAPIRequest": 1,
      "cycleImageFormRequest": 1,
      "cycleImageTotalSize": {
        "jpg": 1,
        "other": 1,
        "png": 1,
        "thumb": 1
      },
      "cycleVideoRequest": 1,
      "cycleVideoTotalLength": {
        "mp4": 1,
        "webm": 1
      },
      "formShare": 1,
      "space": {
        "assets": {},
        "file": {}
      },
      "subscriptionInfo": {
        "end": {},
        "endTrial": {},
        "isTrial": true,
        "type": "string"
      },
      "subscriptionLimit": {
        "isAllowAPI": true,
        "isAllowAPIThumb": true,
        "isAllowAPITransparent": true,
        "isAllowBrandKit": true,
        "isAllowBrandKitColors": true,
        "isAllowBrandKitFonts": true,
        "isAllowBrandKitLogos": true,
        "isAllowDownloadCustomSize": true,
        "isAllowDownloadTransparent": true,
        "isAllowFolder": true,
        "isAllowFormShare": true,
        "isAllowGenerateVideo": true,
        "isAllowTeam": true,
        "isAllowURL": true,
        "maxBandwidthTotal": 1,
        "maxBrandKitFonts": 1,
        "maxFormDownloadRequest": 1,
        "maxFormShare": 1,
        "maxImageAPIRequest": 1,
        "maxImageRequest": 1,
        "maxTemplates": 1,
        "maxVideoLength": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Usage action reference](actions/get-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/duply/latest/actions/get-usage).

## Generate Image

Creates a generated image from a Duply template.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/duply/latest/actions/generate-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "formats[]": [
    "string"
  ],
  "fill": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/duply/latest/actions/generate-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "formats[]": ["string"],
    "fill": {}
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "announcement": "string",
      "files": [
        {
          "filepath": "string",
          "format": "string",
          "size": 1
        }
      ],
      "id": "string",
      "templateId": "string",
      "urls": {
        "filepathJPG": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

See the full [Generate Image action reference](actions/generate-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/duply/latest/actions/generate-image).
