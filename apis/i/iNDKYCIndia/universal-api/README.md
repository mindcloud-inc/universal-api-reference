# <img src="https://images.mindcloud.co/apps/icons/i-ndkycindia_1777396568027.png" alt="IN-D KYC India logo" width="28" height="28"> IN-D KYC India: Universal API

Classify Indian ID documents and extract KYC attributes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iNDKYCIndia/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://in-d.ai/identity-verification/
- **Vendor API docs:** https://dev.in-d.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Classify ID Document](actions/classify-id-document.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/classify-id-document?connectionId=$CONNECTION_ID&filename=sample.png&payload=iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mP8%2Fx8AAwMCAO%2B%2Fp9sAAAAASUVORK5CYII%3D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Connector Documentation

| Action | Method | Description |
| --- | --- | --- |
| [Get Connector Documentation](actions/get-connector-documentation.md) | GET | Retrieves the IN-D KYC India connector documentation. |

### Face Liveness Check

| Action | Method | Description |
| --- | --- | --- |
| [Check Face Liveness](actions/check-face-liveness.md) | GET | Retrieves face liveness results from IN-D KYC India. |
| [Check Face Liveness For UID](actions/check-face-liveness-for-uid.md) | GET | Retrieves face liveness results in IN-D KYC India by UID. |

### Face Match

| Action | Method | Description |
| --- | --- | --- |
| [Match Faces](actions/match-faces.md) | GET | Retrieves face match results from IN-D KYC India. |
| [Match Faces For UID](actions/match-faces-for-uid.md) | GET | Retrieves face match results in IN-D KYC India by UID. |

### Id Document Classification

| Action | Method | Description |
| --- | --- | --- |
| [Classify ID Document](actions/classify-id-document.md) | GET | Retrieves ID document classification results from IN-D KYC India. |
| [Classify ID Documents](actions/classify-id-documents.md) | GET | Retrieves ID document classifications from IN-D KYC India. |
| [Classify ID Documents For UID](actions/classify-id-documents-for-uid.md) | GET | Retrieves ID document classifications in IN-D KYC India by UID. |

### Id Field Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract ID Fields](actions/extract-id-fields.md) | GET | Retrieves extracted ID fields from IN-D KYC India. |
| [Extract ID Fields For UID](actions/extract-id-fields-for-uid.md) | GET | Retrieves extracted ID fields in IN-D KYC India by UID. |

### Id Number Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate ID Number](actions/validate-id-number.md) | GET | Retrieves ID number validation results from IN-D KYC India. |
| [Validate ID Number For UID](actions/validate-id-number-for-uid.md) | GET | Retrieves ID number validation results in IN-D KYC India by UID. |

### Kyc Session

| Action | Method | Description |
| --- | --- | --- |
| [Generate UID](actions/generate-uid.md) | POST | Creates a new KYC session UID in IN-D KYC India. |

### Video Liveness Check

| Action | Method | Description |
| --- | --- | --- |
| [Check Video Liveness](actions/check-video-liveness.md) | GET | Retrieves video liveness results from IN-D KYC India. |
| [Check Video Liveness For UID](actions/check-video-liveness-for-uid.md) | GET | Retrieves video liveness results in IN-D KYC India by UID. |

