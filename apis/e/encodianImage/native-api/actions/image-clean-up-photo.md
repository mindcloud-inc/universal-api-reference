# Image - Clean Up Photo with Encodian - Image

Creates a cleaned-up photo image in Encodian - Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Image/ImageCleanUpPhoto`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Image - Clean Up Photo](https://learn.microsoft.com/en-gb/connectors/encodianimage/#image---clean-up-photo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileName` | body | `string` | yes | The filename of the source image file. The file extension is mandatory. |
| `FileContent` | body | `string` | no | Base64 content of the source image file. |
| `FinalOperation` | body | `boolean` | yes | Return the processed file content instead of only an operation ID. |
| `AutoRotateConfidenceLevel` | body | `number` | yes | Minimum confidence percentage from 0 to 100 used to control whether rotation is applied. |
| `cleanUpType` | body | `list` | no | Clean-up mode to apply. Default performs automatic photo clean-up; None skips clean-up; Specific uses selected advanced clean-up flags. Accepted values: `Default`, `None`, `Specific`. |
| `Deskew` | body | `boolean` | no | Detects the skew angle and rotates to remove that skew. |
| `Despeckle` | body | `boolean` | no | Automatically detects speckles and removes them. |
| `ColorBalance` | body | `boolean` | no | Restores and balances image color quality. |
| `RemoveBorder` | body | `boolean` | no | Locates and removes border pixels from the image. |
| `Contrast` | body | `boolean` | no | Adjusts contrast in the image. |
| `RemoveRedeye` | body | `boolean` | no | Reduces red flash reflection in eyes. |
| `Blur` | body | `boolean` | no | Blurs the image by averaging neighboring pixels. |
| `Diffuse` | body | `boolean` | no | Diffuses the image by replacing pixels with nearby pixels. |
| `Binarize` | body | `boolean` | no | Binarizes the image for dark text on brighter background images. |
| `AutoRotate` | body | `boolean` | no | Automatically detects orientation and rotates the image upright. |
