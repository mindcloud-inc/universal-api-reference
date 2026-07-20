# Add Audio With Subtitle To Video with Bookoly

Adds audio with subtitles to a video in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/add-audio-with-subtitle-to-video`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Add Audio With Subtitle To Video](https://bookoly.com/docs/api/v1#/paths/~1add-audio-with-subtitle-to-video/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video` | body | `object` | yes | — |
| `video.name` | body | `string` | yes | — |
| `video.url` | body | `string` | yes | — |
| `video.mute` | body | `boolean` | yes | — |
| `audio` | body | `object` | yes | — |
| `audio.url` | body | `string` | yes | — |
| `audio.trim` | body | `boolean` | yes | — |
| `audio.volume` | body | `number` | yes | — |
| `subtitle` | body | `object` | yes | — |
| `subtitle.style` | body | `list` | yes | Accepted values: `highlight_current_word`, `rainbow`, `rainbow_highlight_current_word`, `signal`, `signal_highlight_current_word`, `simple`. |
| `subtitle.language` | body | `list` | yes | Accepted values: `af`, `ar`, `az`, `be`, `bg`, `bs`, `ca`, `cs`, `cy`, `da`, `de`, `el`, `en`, `es`, `et`, `fa`, `fi`, `fr`, `gl`, `he`, `hi`, `hr`, `hu`, `hy`, `id`, `is`, `it`, `ja`, `kk`, `kn`, `ko`, `lt`, `lv`, `mi`, `mk`, `mr`, `ms`, `ne`, `nl`, `no`, `pl`, `pt`, `ro`, `ru`, `sk`, `sl`, `sr`, `sv`, `sw`, `ta`, `th`, `tl`, `tr`, `uk`, `ur`, `vi`, `zh`. |
| `font_family` | body | `list` | yes | Accepted values: `Arial`, `Charm`, `Chinese Simplified`, `Chinese Traditional`, `Eagle Lake`, `Korean`, `Korean Bold`, `Libre Baskerville`, `Lobster`, `Luckiest Guy`, `Marck Script`, `Nanum Pen Script`, `Nunito`, `Pacifico`, `Roboto`. |
| `font_size` | body | `number` | yes | — |
| `word_color` | body | `string` | no | — |
| `line_color` | body | `string` | no | — |
| `line_words` | body | `number` | yes | — |
| `outline_width` | body | `number` | yes | — |
| `subtitle.position` | body | `list` | yes | Accepted values: `bottom_center`, `bottom_left`, `bottom_right`, `center_center`, `center_left`, `center_right`, `mid_bottom_center`, `mid_top_center`, `top_center`, `top_left`, `top_right`. |
