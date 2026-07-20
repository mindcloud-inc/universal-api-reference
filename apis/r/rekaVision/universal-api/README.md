# <img src="https://images.mindcloud.co/apps/icons/reka-vision_1775759359697.png" alt="Reka Vision logo" width="28" height="28"> Reka Vision: Universal API

AI video and image analysis for uploads, semantic search, question answering, tagging, clip generation, and derived feature workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rekaVision/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://reka.ai
- **Vendor API docs:** https://docs.reka.ai/vision/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Feature Catalog (V2)](actions/get-feature-catalog-v2.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-feature-catalog-v2?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Caption

| Action | Method | Description |
| --- | --- | --- |
| [List Captions (V2)](actions/list-captions-v2.md) | GET | Retrieves captions from Reka Vision. |

### Feature

| Action | Method | Description |
| --- | --- | --- |
| [Get Feature Catalog (V2)](actions/get-feature-catalog-v2.md) | GET | Retrieves the feature catalog from Reka Vision. |

### Health

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Retrieves the Reka Vision service health status. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Delete Image By Id (V1)](actions/delete-image-by-id-v1.md) | DELETE | Deletes an image from Reka Vision by ID. |
| [Get Image By Id (V1)](actions/get-image-by-id-v1.md) | GET | Retrieves an image from Reka Vision by ID. |
| [List Images (V1)](actions/list-images-v1.md) | GET | Retrieves images from Reka Vision. |
| [Search Images (V1)](actions/search-images-v1.md) | GET | Finds images in Reka Vision by text query. |
| [Upload Images (V1)](actions/upload-images-v1.md) | POST | Uploads images to Reka Vision. |

### Object Detection

| Action | Method | Description |
| --- | --- | --- |
| [List Objects (V2)](actions/list-objects-v2.md) | GET | Retrieves detected objects from Reka Vision. |

### Reel

| Action | Method | Description |
| --- | --- | --- |
| [Create Reel (V1)](actions/create-reel-v1.md) | POST | Creates highlight reels in Reka Vision. |
| [Delete Reel (V1)](actions/delete-reel-v1.md) | DELETE | Deletes a reel generation from Reka Vision. |
| [Get Reel (V1)](actions/get-reel-v1.md) | GET | Retrieves a reel generation status from Reka Vision. |
| [List Reels (V1)](actions/list-reels-v1.md) | GET | Retrieves reel generations from Reka Vision. |

### Scene

| Action | Method | Description |
| --- | --- | --- |
| [List Scenes (V2)](actions/list-scenes-v2.md) | GET | Retrieves scenes from Reka Vision. |

### Transcript

| Action | Method | Description |
| --- | --- | --- |
| [List Transcript (V2)](actions/list-transcript-v2.md) | GET | Retrieves transcript data from Reka Vision. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Delete Video By Id (V1)](actions/delete-video-by-id-v1.md) | DELETE | Deletes a video from Reka Vision by ID. |
| [Delete Video (V2)](actions/delete-video-v2.md) | DELETE | Deletes a video from Reka Vision. |
| [Embedding Search (V1)](actions/embedding-search-v1.md) | GET | Finds video matches in Reka Vision by embedding query. |
| [Get Video By Id (V1)](actions/get-video-by-id-v1.md) | GET | Retrieves a video from Reka Vision by ID. |
| [Get Video (V2)](actions/get-video-v2.md) | GET | Retrieves video details from Reka Vision. |
| [List Videos (V1)](actions/list-videos-v1.md) | GET | Retrieves videos from Reka Vision. |
| [List Videos (V2)](actions/list-videos-v2.md) | GET | Retrieves videos from Reka Vision. |
| [Update Video Metadata (V2)](actions/update-video-metadata-v2.md) | PUT | Updates video metadata in Reka Vision. |
| [Upload Video (V1)](actions/upload-video-v1.md) | POST | Uploads a video to Reka Vision. |
| [Upload Video (V2)](actions/upload-video-v2.md) | POST | Uploads a video to Reka Vision without triggering indexing. |

### Video Feature

| Action | Method | Description |
| --- | --- | --- |
| [Plan Features (V2)](actions/plan-features-v2.md) | GET | Retrieves feature planning results from Reka Vision. |
| [Trigger Captions (V2)](actions/trigger-captions-v2.md) | POST | Creates a captioning job in Reka Vision. |
| [Trigger Embeddings (V2)](actions/trigger-embeddings-v2.md) | POST | Creates an embedding job in Reka Vision. |
| [Trigger Objects (V2)](actions/trigger-objects-v2.md) | POST | Creates an object detection and tracking job in Reka Vision. |
| [Trigger Transcript (V2)](actions/trigger-transcript-v2.md) | POST | Creates a transcript generation job in Reka Vision. |

### Video Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Video Group (V2)](actions/create-video-group-v2.md) | POST | Creates a new video group in Reka Vision. |
| [Delete Video Group (V2)](actions/delete-video-group-v2.md) | DELETE | Deletes an existing video group from Reka Vision. |
| [Get Video Group (V2)](actions/get-video-group-v2.md) | GET | Retrieves a video group from Reka Vision. |
| [List Group Videos (V2)](actions/list-group-videos-v2.md) | GET | Retrieves videos from a Reka Vision group. |
| [List Video Groups (V2)](actions/list-video-groups-v2.md) | GET | Retrieves video groups from Reka Vision. |
| [Move Videos To Group (V2)](actions/move-videos-to-group-v2.md) | PUT | Moves videos to a group in Reka Vision. |
| [Update Video Group (V2)](actions/update-video-group-v2.md) | PUT | Updates an existing video group in Reka Vision. |

### Video Question

| Action | Method | Description |
| --- | --- | --- |
| [Chat (V1)](actions/chat-v1.md) | GET | Retrieves video QA responses from Reka Vision. |

### Video Tag

| Action | Method | Description |
| --- | --- | --- |
| [Indexed Tag (V1)](actions/indexed-tag-v1.md) | GET | Retrieves metadata tags for indexed videos in Reka Vision. |
| [Quick Tag (V1)](actions/quick-tag-v1.md) | POST | Creates metadata tags for short videos in Reka Vision. |

