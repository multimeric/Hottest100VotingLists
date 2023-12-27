# 2021

## How to Download

1. Go to any Hottest 100 page, for example one of the browse pages, and click "View Source". You can shortcut this by just opening <view-source:https://hottest100.abc.net.au/browse/artist/a>
2. Near the bottom of the page there is a line starting with `var officialList =`
3. Copy this line, and strip out anything that is not valid JSON
4. This is then `official.json`

## Format

At a top level, the document is a dictionary mapping track IDs (I guess?) to track objects.
Each track objects has the fields you would expect (`artist`, `title` etc).

Here is an example of the entire document with all but the first song removed:

```json
{
  "1": {
    "id": 1,
    "title": "No Caller ID",
    "artist_name": "1300",
    "track_preview": "A9497CA0-0F5E-4D0E-99FA-4676AC94DA35.mp3",
    "category_id": null,
    "year": null,
    "spotify_track_id": "5tMo7tFM2yPotcIvasyDxQ",
    "apple_track_id": "1560281100",
    "mapi_id": "mtLg0vvrlY",
    "is_official": 1,
    "is_active": 1,
    "merged_track_id": null,
    "created_at": "2021-10-24T18:36:45.000000Z",
    "updated_at": "2021-12-02T02:57:17.000000Z",
    "full_title": "No Caller ID - 1300",
    "artist_name_string": "1300",
    "artists": [
      {
        "id": 1,
        "title": "1300",
        "spotify_artist_id": "34dKvFZNwGaM0NMDtZaJ0P",
        "created_at": "2021-10-24T18:36:45.000000Z",
        "updated_at": "2021-10-24T18:36:45.000000Z",
        "pivot": {
          "track_id": 1,
          "artist_id": 1,
          "order": 0
        }
      }
    ]
  },
}
```