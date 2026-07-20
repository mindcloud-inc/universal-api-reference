# <img src="https://images.mindcloud.co/apps/icons/intervalsicu_1776178372836.png" alt="Intervals.icu logo" width="28" height="28"> Intervals.icu: Universal API

Access Intervals.icu athlete data, training plans, workouts, events, wellness, routes, gear, and related training analytics through the official OpenAPI.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/intervalsicu/latest
- **Actions:** 144
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://intervals.icu
- **Vendor API docs:** https://intervals.icu/api/v1/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Athlete](actions/get-athlete.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/get-athlete?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (144)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Create Activities from File](actions/create-activities-from-file.md) | POST | Creates activities in Intervals.icu from an uploaded file. |
| [Create Manual Activities](actions/create-manual-activities.md) | POST | Creates manual activities in Intervals.icu from external IDs. |
| [Create Manual Activity](actions/create-manual-activity.md) | POST | Creates a manual activity in Intervals.icu. |
| [Delete Activity](actions/delete-activity.md) | DELETE | Deletes an activity from Intervals.icu. |
| [Download Activities CSV](actions/download-activities-csv.md) | GET | Downloads activities from Intervals.icu as CSV. |
| [Find Activities by Intervals](actions/find-activities-by-intervals.md) | GET | Finds activities in Intervals.icu by matching intervals. |
| [Get Activity](actions/get-activity.md) | GET | Retrieves an activity from Intervals.icu. |
| [Get Multiple Activities](actions/get-multiple-activities.md) | GET | Retrieves multiple activities from Intervals.icu. |
| [List Matching Activities](actions/list-matching-activities.md) | GET | Retrieves activities matching sport settings from Intervals.icu. |
| [List Nearby Activities](actions/list-nearby-activities.md) | GET | Retrieves nearby activities from Intervals.icu. |
| [Mark Event Done](actions/mark-event-done.md) | POST | Creates a manual activity from a planned event in Intervals.icu. |
| [Search Full Activities](actions/search-full-activities.md) | GET | Finds full activities in Intervals.icu by name or tag. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an activity in Intervals.icu. |
| [Update Activity Streams](actions/update-activity-streams.md) | PUT | Updates activity streams in Intervals.icu. |
| [Upload Activity Streams CSV](actions/upload-activity-streams-csv.md) | PUT | Updates activity streams in Intervals.icu from CSV. |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from Intervals.icu. |
| [Search Activities](actions/search-activities.md) | GET | Finds activities in Intervals.icu by name or tag. |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Gear](actions/create-gear.md) | POST | Creates gear in Intervals.icu. |
| [Delete Gear](actions/delete-gear.md) | DELETE | Deletes gear from Intervals.icu. |
| [List Athlete Gear](actions/list-athlete-gear.md) | GET | Retrieves athlete gear from Intervals.icu. |
| [Replace Gear](actions/replace-gear.md) | POST | Replaces gear in Intervals.icu. |
| [Update Gear](actions/update-gear.md) | PUT | Updates gear in Intervals.icu. |

### Athlete

| Action | Method | Description |
| --- | --- | --- |
| [Get Athlete](actions/get-athlete.md) | GET | Retrieves an athlete from Intervals.icu. |

### Athlete Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Athlete Profile](actions/get-athlete-profile.md) | GET | Retrieves an athlete profile from Intervals.icu. |

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [Apply Event Plan](actions/apply-event-plan.md) | POST | Applies a workout plan in Intervals.icu. |
| [Bulk Delete Events](actions/bulk-delete-events.md) | PUT | Deletes calendar events in Intervals.icu by ID or external ID. |
| [Create Event](actions/create-event.md) | POST | Creates a calendar event in Intervals.icu. |
| [Create Events](actions/create-events.md) | POST | Creates calendar events in Intervals.icu. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes a calendar event from Intervals.icu. |
| [Delete Events in Range](actions/delete-events-in-range.md) | DELETE | Deletes calendar events from Intervals.icu. |
| [Duplicate Events](actions/duplicate-events.md) | POST | Duplicates calendar events in Intervals.icu. |
| [Get Event](actions/get-event.md) | GET | Retrieves a calendar event from Intervals.icu. |
| [Get Shared Event](actions/get-shared-event.md) | GET | Retrieves a shared event from Intervals.icu. |
| [Update Event](actions/update-event.md) | PUT | Updates a calendar event in Intervals.icu. |
| [Update Events](actions/update-events.md) | PUT | Updates calendar events in Intervals.icu. |

### Custom Item

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Items](actions/list-custom-items.md) | GET | Retrieves custom items from Intervals.icu. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves calendar events from Intervals.icu. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET | Retrieves workout folders from Intervals.icu. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a workout folder in Intervals.icu. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes a workout folder from Intervals.icu. |
| [Update Folder](actions/update-folder.md) | PUT | Updates a workout folder in Intervals.icu. |
| [Update Folder Sharing](actions/update-folder-sharing.md) | PUT | Updates folder sharing in Intervals.icu. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Activity Message](actions/add-activity-message.md) | POST | Adds an activity message in Intervals.icu. |
| [Apply Plan Changes](actions/apply-plan-changes.md) | PUT | Applies plan changes to an athlete calendar in Intervals.icu. |
| [Apply Sport Settings](actions/apply-sport-settings.md) | PUT | Applies sport settings to activities in Intervals.icu. |
| [Compare Route Similarity](actions/compare-route-similarity.md) | GET | Compares route similarity in Intervals.icu. |
| [Create Custom Item](actions/create-custom-item.md) | POST | Creates a custom item in Intervals.icu. |
| [Create Gear Reminder](actions/create-gear-reminder.md) | POST | Creates a gear reminder in Intervals.icu. |
| [Create Sport Settings](actions/create-sport-settings.md) | POST | Creates sport settings in Intervals.icu. |
| [Create Workout](actions/create-workout.md) | POST | Creates a workout in Intervals.icu. |
| [Create Workouts](actions/create-workouts.md) | POST | Creates workouts in Intervals.icu. |
| [Delete Chat Message](actions/delete-chat-message.md) | DELETE | Deletes a chat message from Intervals.icu. |
| [Delete Custom Item](actions/delete-custom-item.md) | DELETE | Deletes a custom item from Intervals.icu. |
| [Delete Gear Reminder](actions/delete-gear-reminder.md) | DELETE | Deletes a gear reminder from Intervals.icu. |
| [Delete Intervals](actions/delete-intervals.md) | PUT | Deletes activity intervals from Intervals.icu. |
| [Delete Sport Settings](actions/delete-sport-settings.md) | DELETE | Deletes sport settings from Intervals.icu. |
| [Delete Workout](actions/delete-workout.md) | DELETE | Deletes a workout from Intervals.icu. |
| [Disconnect App](actions/disconnect-app.md) | DELETE | Disconnects an app from Intervals.icu. |
| [Download Activity File](actions/download-activity-file.md) | GET | Downloads an activity file from Intervals.icu. |
| [Download Activity FIT File](actions/download-activity-fit-file.md) | GET | Downloads an activity FIT file from Intervals.icu. |
| [Download Activity FIT Files](actions/download-activity-fit-files.md) | POST | Downloads activity FIT files from Intervals.icu as a ZIP. |
| [Download Activity GPX File](actions/download-activity-gpx-file.md) | GET | Downloads an activity GPX file from Intervals.icu. |
| [Download Event Workout](actions/download-event-workout.md) | GET | Downloads a planned workout from Intervals.icu. |
| [Download Workout](actions/download-workout.md) | POST | Converts a workout file in Intervals.icu. |
| [Download Workout File](actions/download-workout-file.md) | POST | Converts a workout file in Intervals.icu. |
| [Download Workouts ZIP](actions/download-workouts-zip.md) | GET | Downloads workout files from Intervals.icu as a ZIP. |
| [Duplicate Workouts](actions/duplicate-workouts.md) | POST | Duplicates workouts in Intervals.icu. |
| [Find Best Efforts](actions/find-best-efforts.md) | GET | Finds best efforts in an Intervals.icu activity. |
| [Get Activity Heart Rate Curve](actions/get-activity-heart-rate-curve.md) | GET | Retrieves an activity heart rate curve from Intervals.icu. |
| [Get Activity Heart Rate Curves](actions/get-activity-heart-rate-curves.md) | GET | Retrieves matching activity heart rate curves from Intervals.icu. |
| [Get Activity Intervals](actions/get-activity-intervals.md) | GET | Retrieves activity intervals from Intervals.icu. |
| [Get Activity Map](actions/get-activity-map.md) | GET | Retrieves an activity map from Intervals.icu. |
| [Get Activity Pace Curve](actions/get-activity-pace-curve.md) | GET | Retrieves an activity pace curve from Intervals.icu. |
| [Get Activity Pace Curves](actions/get-activity-pace-curves.md) | GET | Retrieves matching activity pace curves from Intervals.icu. |
| [Get Activity Power Curve](actions/get-activity-power-curve.md) | GET | Retrieves an activity power curve from Intervals.icu. |
| [Get Activity Power Curves](actions/get-activity-power-curves.md) | GET | Retrieves matching activity power curves from Intervals.icu. |
| [Get Activity Power Spike Model](actions/get-activity-power-spike-model.md) | GET | Retrieves an activity power spike model from Intervals.icu. |
| [Get Activity Segments](actions/get-activity-segments.md) | GET | Retrieves activity segments from Intervals.icu. |
| [Get Activity Streams](actions/get-activity-streams.md) | GET | Retrieves activity streams from Intervals.icu. |
| [Get Activity Weather Summary](actions/get-activity-weather-summary.md) | GET | Retrieves an activity weather summary from Intervals.icu. |
| [Get Athlete Power vs Heart Rate Curve](actions/get-athlete-power-vs-heart-rate-curve.md) | GET | Retrieves power versus heart rate curves from Intervals.icu. |
| [Get Athlete Settings](actions/get-athlete-settings.md) | GET | Retrieves athlete device settings from Intervals.icu. |
| [Get Athlete Summary](actions/get-athlete-summary.md) | GET | Retrieves athlete summary information from Intervals.icu. |
| [Get Chat](actions/get-chat.md) | GET | Retrieves a chat from Intervals.icu. |
| [Get Custom Item](actions/get-custom-item.md) | GET | Retrieves a custom item from Intervals.icu. |
| [Get Gap Histogram](actions/get-gap-histogram.md) | GET | Retrieves an activity gap histogram from Intervals.icu. |
| [Get Heart Rate Histogram](actions/get-heart-rate-histogram.md) | GET | Retrieves a heart rate histogram from Intervals.icu. |
| [Get Heart Rate Training Load Model](actions/get-heart-rate-training-load-model.md) | GET | Retrieves a heart rate training load model from Intervals.icu. |
| [Get Interval Stats](actions/get-interval-stats.md) | GET | Retrieves interval statistics from Intervals.icu. |
| [Get MMP Model](actions/get-mmp-model.md) | GET | Retrieves an athlete power model from Intervals.icu. |
| [Get Pace Histogram](actions/get-pace-histogram.md) | GET | Retrieves a pace histogram from Intervals.icu. |
| [Get Power Histogram](actions/get-power-histogram.md) | GET | Retrieves a power histogram from Intervals.icu. |
| [Get Power vs Heart Rate](actions/get-power-vs-heart-rate.md) | GET | Retrieves power versus heart rate data from Intervals.icu. |
| [Get Route](actions/get-route.md) | GET | Retrieves a route from Intervals.icu. |
| [Get Sport Settings](actions/get-sport-settings.md) | GET | Retrieves sport settings from Intervals.icu. |
| [Get Time at Heart Rate](actions/get-time-at-heart-rate.md) | GET | Retrieves time at heart rate data from Intervals.icu. |
| [Get Training Plan](actions/get-training-plan.md) | GET | Retrieves an athlete training plan from Intervals.icu. |
| [Get Weather Configuration](actions/get-weather-configuration.md) | GET | Retrieves weather forecast settings from Intervals.icu. |
| [Get Weather Forecast](actions/get-weather-forecast.md) | GET | Retrieves weather forecast information from Intervals.icu. |
| [Get Wellness Record](actions/get-wellness-record.md) | GET | Retrieves a wellness record from Intervals.icu. |
| [Get Workout](actions/get-workout.md) | GET | Retrieves a workout from Intervals.icu. |
| [Import Workout](actions/import-workout.md) | POST | Creates a workout in Intervals.icu from an imported file. |
| [List Activity Messages](actions/list-activity-messages.md) | GET | Retrieves activity messages from Intervals.icu. |
| [List Activity Power Curves](actions/list-activity-power-curves.md) | GET | Retrieves activity power curves from Intervals.icu. |
| [List Activity Tags](actions/list-activity-tags.md) | GET | Retrieves activity tags from Intervals.icu. |
| [List Athlete Chats](actions/list-athlete-chats.md) | GET | Retrieves athlete chats from Intervals.icu. |
| [List Chat Messages](actions/list-chat-messages.md) | GET | Retrieves chat messages from Intervals.icu. |
| [List Event Tags](actions/list-event-tags.md) | GET | Retrieves event tags from Intervals.icu. |
| [List Fitness Model Events](actions/list-fitness-model-events.md) | GET | Retrieves fitness model events from Intervals.icu. |
| [List Global Pace Distances](actions/list-global-pace-distances.md) | GET | Retrieves pace distances from Intervals.icu. |
| [List Heart Rate Curves](actions/list-heart-rate-curves.md) | GET | Retrieves athlete heart rate curves from Intervals.icu. |
| [List Pace Curves](actions/list-pace-curves.md) | GET | Retrieves athlete pace curves from Intervals.icu. |
| [List Pace Distances](actions/list-pace-distances.md) | GET | Retrieves pace distances from Intervals.icu. |
| [List Power Curves](actions/list-power-curves.md) | GET | Retrieves athlete power curves from Intervals.icu. |
| [List Routes](actions/list-routes.md) | GET | Retrieves routes from Intervals.icu. |
| [List Shared Folder Athletes](actions/list-shared-folder-athletes.md) | GET | Retrieves athletes sharing a folder in Intervals.icu. |
| [List Sport Settings](actions/list-sport-settings.md) | GET | Retrieves sport settings from Intervals.icu. |
| [List Wellness Records](actions/list-wellness-records.md) | GET | Retrieves wellness records from Intervals.icu. |
| [List Workout Tags](actions/list-workout-tags.md) | GET | Retrieves workout tags from Intervals.icu. |
| [Recalculate Gear Stats](actions/recalculate-gear-stats.md) | GET | Recalculates gear stats in Intervals.icu. |
| [Reorder Custom Items](actions/reorder-custom-items.md) | PUT | Reorders custom items in Intervals.icu. |
| [Send Message](actions/send-message.md) | POST | Sends a chat message in Intervals.icu. |
| [Split Interval](actions/split-interval.md) | PUT | Splits an interval in Intervals.icu. |
| [Update Athlete Plans](actions/update-athlete-plans.md) | PUT | Updates athlete training plans in Intervals.icu. |
| [Update Chat Message](actions/update-chat-message.md) | PUT | Updates a chat message in Intervals.icu. |
| [Update Custom Item](actions/update-custom-item.md) | PUT | Updates a custom item in Intervals.icu. |
| [Update Gear Reminder](actions/update-gear-reminder.md) | PUT | Updates a gear reminder in Intervals.icu. |
| [Update Interval](actions/update-interval.md) | PUT | Updates an interval in Intervals.icu. |
| [Update Intervals](actions/update-intervals.md) | PUT | Updates activity intervals in Intervals.icu. |
| [Update Last Seen Message](actions/update-last-seen-message.md) | PUT | Updates a chat last seen message in Intervals.icu. |
| [Update Multiple Sport Settings](actions/update-multiple-sport-settings.md) | PUT | Updates multiple sport settings in Intervals.icu. |
| [Update Plan Workouts](actions/update-plan-workouts.md) | PUT | Updates plan workouts in Intervals.icu. |
| [Update Route](actions/update-route.md) | PUT | Updates a route in Intervals.icu. |
| [Update Sport Settings](actions/update-sport-settings.md) | PUT | Updates sport settings in Intervals.icu. |
| [Update Training Plan](actions/update-training-plan.md) | PUT | Updates an athlete training plan in Intervals.icu. |
| [Update Weather Configuration](actions/update-weather-configuration.md) | PUT | Updates weather forecast settings in Intervals.icu. |
| [Update Wellness Record](actions/update-wellness-record.md) | PUT | Updates a wellness record in Intervals.icu. |
| [Update Wellness Record by Date](actions/update-wellness-record-by-date.md) | PUT | Updates a wellness record in Intervals.icu. |
| [Update Wellness Records Bulk](actions/update-wellness-records-bulk.md) | PUT | Updates wellness records in Intervals.icu. |
| [Update Workout](actions/update-workout.md) | PUT | Updates a workout in Intervals.icu. |
| [Upload Custom Item Image](actions/upload-custom-item-image.md) | POST | Uploads a custom item image to Intervals.icu. |
| [Upload Wellness Records](actions/upload-wellness-records.md) | POST | Uploads wellness records to Intervals.icu. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Update Athlete](actions/update-athlete.md) | PUT | Updates an athlete in Intervals.icu. |

### Workout

| Action | Method | Description |
| --- | --- | --- |
| [List Workouts](actions/list-workouts.md) | GET | Retrieves workouts from Intervals.icu. |

