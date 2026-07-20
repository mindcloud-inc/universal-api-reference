# Image - Clean Up Document with Encodian - Image

Creates a cleaned-up document image in Encodian - Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Image/ImageCleanUpDocument`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Image - Clean Up Document](https://learn.microsoft.com/en-gb/connectors/encodianimage/#image---clean-up-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileName` | body | `string` | yes | The filename of the source image file. The file extension is mandatory. |
| `FileContent` | body | `string` | no | Base64 content of the source image file. |
| `FinalOperation` | body | `boolean` | yes | Return the processed file content instead of only an operation ID. |
| `AutoRotateConfidenceLevel` | body | `number` | yes | Minimum confidence percentage from 0 to 100 used to control whether rotation is applied. |
| `cleanUpType` | body | `list` | no | Clean-up mode to apply. Default performs automatic document clean-up; None skips clean-up; Specific uses selected advanced clean-up flags. Accepted values: `Default`, `None`, `Specific`. |
| `AutoRotate` | body | `boolean` | no | Automatically detects orientation and rotates the image upright. |
| `Deskew` | body | `boolean` | no | Detects the skew angle and rotates to remove that skew. |
| `Despeckle` | body | `boolean` | no | Automatically detects speckles and removes them. |
| `AdjustBrightnessContrast` | body | `boolean` | no | Automatically adjusts brightness and contrast based on image analysis. |
| `RemoveBorder` | body | `boolean` | no | Locates and removes border pixels from the document. |
| `SmoothBackground` | body | `boolean` | no | Smooths background colors to reduce noise. |
| `SmoothObjects` | body | `boolean` | no | Smooths object edges in bitonal documents. |
| `RemoveDotShading` | body | `boolean` | no | Removes shaded regions from bitonal documents. |
| `ImageDetergent` | body | `boolean` | no | Smooths regions by shifting similar color values toward a central value. |
| `ApplyAverageFilter` | body | `boolean` | no | Applies a 3x3 average filter smoothing operation. |
| `RemoveHolePunch` | body | `boolean` | no | Detects and removes hole punch marks from a bitonal document. |
| `Binarize` | body | `boolean` | no | Binarizes the image for dark text on brighter background documents. |
