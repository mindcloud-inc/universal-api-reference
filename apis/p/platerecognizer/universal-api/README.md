# <img src="https://images.mindcloud.co/apps/icons/orig_1775582715535.jpeg" alt="Platerecognizer logo" width="28" height="28"> Platerecognizer: Universal API

Production-ready wrapper for Plate Recognizer cloud APIs across Snapshot, OCR, VIN ID, VisionAlert, Stream Cloud, and Blur with apiKey auth.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/platerecognizer/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://platerecognizer.com
- **Vendor API docs:** https://guides.platerecognizer.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Statistics](actions/get-statistics.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/get-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Blur Result

| Action | Method | Description |
| --- | --- | --- |
| [Blur Plates And Faces In Image](actions/blur-plates-and-faces-in-image.md) | GET | Blurs plates and faces in an image with Plate Recognizer. |

### Camera Monitoring Log

| Action | Method | Description |
| --- | --- | --- |
| [Create Camera Monitoring Log](actions/create-camera-monitoring-log.md) | POST | Creates a camera monitoring log in Plate Recognizer VisionAlert. |

### Ocr Result

| Action | Method | Description |
| --- | --- | --- |
| [Extract Text From Image](actions/extract-text-from-image.md) | GET | Extracts text from an image with Plate Recognizer OCR. |

### Plate Recognition

| Action | Method | Description |
| --- | --- | --- |
| [Read Number Plates From Image](actions/read-number-plates-from-image.md) | GET | Reads vehicle number plates from an image with Plate Recognizer. |

### Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get OCR Statistics](actions/get-ocr-statistics.md) | GET | Retrieves your Plate Recognizer OCR usage statistics. |
| [Get Statistics](actions/get-statistics.md) | GET | Retrieves your Plate Recognizer Snapshot usage statistics. |
| [Get VIN Statistics](actions/get-vin-statistics.md) | GET | Retrieves your Plate Recognizer VIN ID usage statistics. |

### Video Upload

| Action | Method | Description |
| --- | --- | --- |
| [Upload Video For Stream Cloud](actions/upload-video-for-stream-cloud.md) | POST | Uploads a video to Plate Recognizer Stream Cloud. |

### Vin

| Action | Method | Description |
| --- | --- | --- |
| [Read VIN From Image](actions/read-vin-from-image.md) | GET | Reads a VIN from an image with Plate Recognizer. |

