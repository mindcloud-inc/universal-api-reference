# Image - Extract Text with Encodian - Image

Retrieves text from an image in Encodian - Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Image/ImageExtractText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Image - Extract Text](https://support.encodian.com/hc/en-gb/articles/360006998078-Extract-Text-from-Image-OCR)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileName` | body | `string` | yes | The filename of the source image file. |
| `imageType` | body | `list` | yes | Source image file format for OCR processing. Accepted values: `BMP`, `JPG`, `PNG`, `TIFF`. |
| `fileContent` | body | `string` | yes | Base64 content of the source image file. |
| `AutoRotateConfidenceLevel` | body | `number` | yes | Minimum confidence percentage from 0 to 100 used to control whether rotation is applied. |
| `ocrLanguage` | body | `list` | no | Language used for OCR processing. Default is English. Accepted values: `Albanian`, `Arabic`, `Azerbaijani`, `Basque`, `Belarusian`, `Bengali`, `Bosnian`, `Bulgarian`, `Burmese`, `Catalan`, `ChineseSimplified`, `ChineseTraditional`, `Croatian`, `Czech`, `Danish`, `Dutch`, `English`, `Estonian`, `Finnish`, `French`, `Georgian`, `German`, `Greek`, `Gujarati`, `Hebrew`, `Hindi`, `Hungarian`, `Icelandic`, `Indonesian`, `Italian`, `Japanese`, `Kannada`, `Kazakh`, `Khmer`, `Korean`, `Kurdish`, `Kyrgyz`, `Laotian`, `Latin`, `Latvian`, `Lithuanian`, `Macedonian`, `Maharashtra`, `Malay`, `Malayalam`, `Maltese`, `Nepali`, `Norwegian`, `Oriya`, `Panjabi`, `Persian`, `Polish`, `Portuguese`, `Pushto`, `Romanian`, `Russian`, `Sanskrit`, `Serbian`, `Singhalese`, `Slovakian`, `Slovenian`, `Spanish`, `Swahili`, `Swedish`, `Syriac`, `Tamil`, `Telugu`, `Thai`, `Turkish`, `Ukrainian`, `Urdu`, `Uzbek`, `Vietnamese`, `Welsh`, `Yiddish`. |
| `cleanUpType` | body | `list` | no | Clean-up mode to apply before OCR processing. Default performs automatic clean-up; None skips clean-up; Specific uses selected advanced clean-up flags. Accepted values: `Default`, `None`, `Specific`. |
| `AutoRotate` | body | `boolean` | no | Automatically detects orientation and rotates the image upright before OCR. |
| `Deskew` | body | `boolean` | no | Detects the skew angle and rotates to remove that skew before OCR. |
| `Despeckle` | body | `boolean` | no | Automatically detects speckles and removes them before OCR. |
| `AdjustBrightnessContrast` | body | `boolean` | no | Automatically adjusts brightness and contrast before OCR. |
| `RemoveBorder` | body | `boolean` | no | Locates and removes border pixels before OCR. |
| `SmoothBackground` | body | `boolean` | no | Smooths background colors to reduce noise before OCR. |
| `SmoothObjects` | body | `boolean` | no | Smooths object edges in bitonal documents before OCR. |
| `RemoveDotShading` | body | `boolean` | no | Removes shaded regions from bitonal documents before OCR. |
| `ImageDetergent` | body | `boolean` | no | Smooths regions by shifting similar color values toward a central value before OCR. |
| `ApplyAverageFilter` | body | `boolean` | no | Applies a 3x3 average filter smoothing operation before OCR. |
| `RemoveHolePunch` | body | `boolean` | no | Detects and removes hole punch marks before OCR. |
| `Binarize` | body | `boolean` | no | Binarizes the image before OCR. |
