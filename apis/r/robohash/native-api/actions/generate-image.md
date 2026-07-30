# Generate Image with Robohash

## Endpoint

- **Method:** `GET`
- **Path:** `/:text.:format`
- **Base URL:** `https://robohash.org`
- **Official documentation:** [Generate Image](https://github.com/e1ven/Robohash)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | path | `string` | yes | Text value used to deterministically generate the Robohash image. |
| `format` | path | `list` | yes | Image file extension documented by Robohash, such as png or jpg. Accepted values: `bmp`, `jpg`, `png`. |
| `size` | query | `string` | no | Optional image dimensions in WIDTHxHEIGHT format, for example 200x200. |
| `set` | query | `list` | no | Optional image set. Official provider documentation and its README list set1 through set6 and any. Accepted values: `any`, `set1`, `set2`, `set3`, `set4`, `set5`, `set6`. |
| `bgset` | query | `list` | no | Optional background set. Official public docs list bg1, bg2, or any. Accepted values: `any`, `bg1`, `bg2`. |
| `gravatar` | query | `list` | no | Optional Gravatar behavior. Use yes for an email value, or hashed for a pre-hashed email value. Accepted values: `hashed`, `yes`. |
| `ignoreext` | query | `boolean` | no | Set to false when the extension should be included in the hashed text value. |
| `sets` | query | `string` | no | Optional comma-delimited set numbers, for example 1,3. The provider documents explicit set lists as stable compared with set=any. |
