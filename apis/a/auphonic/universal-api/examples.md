# Auphonic Universal API Examples

These examples use the MindCloud API key and Auphonic connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User Account Info

Retrieves current user account info from Auphonic.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-current-user-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-current-user-account-info?${params}`, {
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
      "credits": 1,
      "dateJoined": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "errorEmail": true,
      "lowCreditsEmail": true,
      "lowCreditsThreshold": 1,
      "notificationEmail": true,
      "onetimeCredits": 1,
      "rechargeDate": "2026-05-07T12:00:00.000Z",
      "rechargeRecurringCredits": 1,
      "recurringCredits": 1,
      "userId": "string",
      "username": "Ava Chen",
      "warningEmail": true
    }
  ],
  "meta": {}
}
```

See the full [Get Current User Account Info action reference](actions/get-current-user-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/auphonic/latest/actions/get-current-user-account-info).

## Create Preset

Creates a new preset in Auphonic.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/create-preset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "presetName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/create-preset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "presetName": "Ava Chen"
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
      "algorithms": {
        "compressorMusic": "string",
        "compressorSpeech": "string",
        "coughCutter": true,
        "cutMode": "string",
        "cutter": true,
        "debreathamount": 1,
        "dehum": 1,
        "dehumamount": 1,
        "denoise": true,
        "denoiseamount": 1,
        "denoisemethod": "string",
        "deverbamount": 1,
        "dualmono": true,
        "fillerCutter": true,
        "filtering": true,
        "filtermethod": "string",
        "leveler": true,
        "levelermode": "string",
        "levelerstrengthMusic": 1,
        "levelerstrengthSpeech": 1,
        "loudnessmethod": "string",
        "loudnesstarget": 1,
        "maxlra": 1,
        "maxm": 1,
        "maxpeak": 1,
        "maxs": 1,
        "msclassifier": "string",
        "musicCutter": true,
        "musicgain": 1,
        "normloudness": true,
        "silenceCutter": true
      },
      "creationTime": "2026-05-07T12:00:00.000Z",
      "image": {},
      "isMultitrack": true,
      "metadata": {
        "album": "string",
        "appendChapters": true,
        "artist": "string",
        "genre": "string",
        "license": "string",
        "licenseUrl": "https://example.com",
        "location": {
          "latitude": {},
          "longitude": {}
        },
        "publisher": "string",
        "subtitle": "string",
        "summary": "string",
        "tags": [
          "string"
        ],
        "title": "string",
        "track": "string",
        "url": "https://example.com",
        "year": "string"
      },
      "outputBasename": "Ava Chen",
      "presetName": "Ava Chen",
      "reviewBeforePublishing": true,
      "speechRecognition": {},
      "thumbnail": {},
      "uuid": "string",
      "webhook": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Preset action reference](actions/create-preset.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/auphonic/latest/actions/create-preset).
