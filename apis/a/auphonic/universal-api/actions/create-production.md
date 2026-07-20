# Auphonic: Create Production

Creates a new production in Auphonic.

```
POST https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/create-production
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auphonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/create-production" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "preset": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/create-production', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "preset": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `preset` | string | yes | Preset UUID or preset name to use as the production template. |
| `action` | list | no | Set to start to process the production immediately. One of: `start`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputFile` | string | no | HTTP URL or external-service filename for the input media. |
| `isMultitrack` | boolean | no | Create the production as multitrack. |

## Response

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
      "bitrate": {},
      "changeAllowed": true,
      "changeTime": "2026-05-07T12:00:00.000Z",
      "channels": {},
      "creationTime": "2026-05-07T12:00:00.000Z",
      "cutEnd": 1,
      "cutStart": 1,
      "editPage": "string",
      "errorMessage": "string",
      "errorStatus": {},
      "format": "string",
      "hasVideo": true,
      "image": {},
      "inputFile": "string",
      "inReview": true,
      "isMultitrack": true,
      "length": 1,
      "lengthTimestring": "string",
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
      "preset": "string",
      "reviewBeforePublishing": true,
      "samplerate": {},
      "service": {},
      "shownotes": {},
      "speechRecognition": {},
      "startAllowed": true,
      "statistics": {},
      "status": 1,
      "statusPage": "string",
      "statusString": "string",
      "thumbnail": {},
      "usedCredits": {},
      "uuid": "string",
      "warningMessage": "string",
      "warningStatus": {},
      "waveformImage": "string",
      "webhook": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `algorithms.compressorMusic` | string |  |
| `algorithms.compressorSpeech` | string |  |
| `algorithms.coughCutter` | boolean |  |
| `algorithms.cutMode` | string |  |
| `algorithms.cutter` | boolean |  |
| `algorithms.debreathamount` | number |  |
| `algorithms.dehum` | number |  |
| `algorithms.dehumamount` | number |  |
| `algorithms.denoise` | boolean |  |
| `algorithms.denoiseamount` | number |  |
| `algorithms.denoisemethod` | string |  |
| `algorithms.deverbamount` | number |  |
| `algorithms.dualmono` | boolean |  |
| `algorithms.fillerCutter` | boolean |  |
| `algorithms.filtering` | boolean |  |
| `algorithms.filtermethod` | string |  |
| `algorithms.leveler` | boolean |  |
| `algorithms.levelermode` | string |  |
| `algorithms.levelerstrengthMusic` | number |  |
| `algorithms.levelerstrengthSpeech` | number |  |
| `algorithms.loudnessmethod` | string |  |
| `algorithms.loudnesstarget` | number |  |
| `algorithms.maxlra` | number |  |
| `algorithms.maxm` | number |  |
| `algorithms.maxpeak` | number |  |
| `algorithms.maxs` | number |  |
| `algorithms.msclassifier` | string |  |
| `algorithms.musicCutter` | boolean |  |
| `algorithms.musicgain` | number |  |
| `algorithms.normloudness` | boolean |  |
| `algorithms.silenceCutter` | boolean |  |
| `bitrate` | object |  |
| `changeAllowed` | boolean |  |
| `changeTime` | date |  |
| `channels` | object |  |
| `creationTime` | date |  |
| `cutEnd` | number |  |
| `cutStart` | number |  |
| `editPage` | string |  |
| `errorMessage` | string |  |
| `errorStatus` | object |  |
| `format` | string |  |
| `hasVideo` | boolean |  |
| `image` | object |  |
| `inputFile` | string |  |
| `inReview` | boolean |  |
| `isMultitrack` | boolean |  |
| `length` | number |  |
| `lengthTimestring` | string |  |
| `metadata.album` | string |  |
| `metadata.appendChapters` | boolean |  |
| `metadata.artist` | string |  |
| `metadata.genre` | string |  |
| `metadata.license` | string |  |
| `metadata.licenseUrl` | string |  |
| `metadata.location.latitude` | object |  |
| `metadata.location.longitude` | object |  |
| `metadata.publisher` | string |  |
| `metadata.subtitle` | string |  |
| `metadata.summary` | string |  |
| `metadata.tags[]` | string |  |
| `metadata.title` | string |  |
| `metadata.track` | string |  |
| `metadata.url` | string |  |
| `metadata.year` | string |  |
| `outputBasename` | string |  |
| `preset` | string |  |
| `reviewBeforePublishing` | boolean |  |
| `samplerate` | object |  |
| `service` | object |  |
| `shownotes` | object |  |
| `speechRecognition` | object |  |
| `startAllowed` | boolean |  |
| `statistics` | object |  |
| `status` | number |  |
| `statusPage` | string |  |
| `statusString` | string |  |
| `thumbnail` | object |  |
| `usedCredits` | object |  |
| `uuid` | string |  |
| `warningMessage` | string |  |
| `warningStatus` | object |  |
| `waveformImage` | string |  |
| `webhook` | object |  |

## Native endpoint

Through the native Auphonic API, this operation is `POST /productions.json` (base URL `https://auphonic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-production.md) for the provider-specific parameters and requirements.

