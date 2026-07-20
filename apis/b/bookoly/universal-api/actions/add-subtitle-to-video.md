# Bookoly: Add Subtitle To Video

Adds subtitles to a video in Bookoly.

```
POST https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/add-subtitle-to-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookoly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/add-subtitle-to-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video": {},
  "video.name": "Ava Chen",
  "video.url": "https://example.com",
  "subtitle": {},
  "subtitle.style": "highlight_current_word",
  "subtitle.language": "af",
  "subtitle.font_family": "Arial",
  "subtitle.font_size": 1,
  "subtitle.line_words": 1,
  "subtitle.outline_width": 1,
  "subtitle.position": "bottom_center"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/add-subtitle-to-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "video": {},
    "video.name": "Ava Chen",
    "video.url": "https://example.com",
    "subtitle": {},
    "subtitle.style": "highlight_current_word",
    "subtitle.language": "af",
    "subtitle.font_family": "Arial",
    "subtitle.font_size": 1,
    "subtitle.line_words": 1,
    "subtitle.outline_width": 1,
    "subtitle.position": "bottom_center"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `video` | object | yes |  |
| `video.name` | string | yes |  |
| `video.url` | string | yes |  |
| `subtitle` | object | yes |  |
| `subtitle.style` | list | yes | One of: `highlight_current_word`, `rainbow`, `rainbow_highlight_current_word`, `signal`, `signal_highlight_current_word`, `simple`. |
| `subtitle.language` | list | yes | One of: `af`, `ar`, `az`, `be`, `bg`, `bs`, `ca`, `cs`, `cy`, `da`, `de`, `el`, `en`, `es`, `et`, `fa`, `fi`, `fr`, `gl`, `he`, `hi`, `hr`, `hu`, `hy`, `id`, `is`, `it`, `ja`, `kk`, `kn`, `ko`, `lt`, `lv`, `mi`, `mk`, `mr`, `ms`, `ne`, `nl`, `no`, `pl`, `pt`, `ro`, `ru`, `sk`, `sl`, `sr`, `sv`, `sw`, `ta`, `th`, `tl`, `tr`, `uk`, `ur`, `vi`, `zh`. |
| `subtitle.font_family` | list | yes | One of: `Arial`, `Charm`, `Chinese Simplified`, `Chinese Traditional`, `Eagle Lake`, `Korean`, `Korean Bold`, `Libre Baskerville`, `Lobster`, `Luckiest Guy`, `Marck Script`, `Nanum Pen Script`, `Nunito`, `Pacifico`, `Roboto`. |
| `subtitle.font_size` | number | yes |  |
| `subtitle.word_color` | string | no |  |
| `subtitle.line_color` | string | no |  |
| `subtitle.line_words` | number | yes |  |
| `subtitle.outline_width` | number | yes |  |
| `subtitle.position` | list | yes | One of: `bottom_center`, `bottom_left`, `bottom_right`, `center_center`, `center_left`, `center_right`, `mid_bottom_center`, `mid_top_center`, `top_center`, `top_left`, `top_right`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bookoly API returns.

## Native endpoint

Through the native Bookoly API, this operation is `POST /add-subtitle-to-video` (base URL `https://bookoly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-subtitle-to-video.md) for the provider-specific parameters and requirements.

