# YouTube long-form editing data (2026)

Open datasets from **Kevin Tabares** (long-form YouTube editor, [Umbrella Creators](https://umbrellacreators.com)).
Free to use with attribution: "Kevin Tabares, Umbrella Creators (umbrellacreators.com)".

## 1. `loudness-2026/` — How loud are big YouTube channels?

50 long-form videos from 25 large channels, measured in 2026: integrated loudness (LUFS), true peak, duration and speaking pace.

- Median loudness: **-16.3 LUFS** (range -24.3 to -7.4). 12 of 50 videos were louder than -14 LUFS.
- Write-up and method: https://umbrellacreators.com/blog/youtube-loudness-lufs-study-2026

## 2. `roblox-long-form-2026/` — 1,142 Roblox and Minecraft long-form videos

Every long-form video Kevin edited between 2025-01-01 and 2026-10-02 for 42 channels (MudPlayz, ashlele, Puff, Rex & Alexa, DakBlox, Crazz, HyperCookiie and others), with title features and the view count shown on YT Jobs on 2026-10-02.

- Source: Kevin's YT Jobs profile (https://ytjobs.co/@kevintabaress).
- **Caveat:** views are cumulative on the extraction date, so older videos had more time to collect views. Use for description and correlation, not causation. Views depend on topic, title, thumbnail and timing, not only on the edit.
- Write-up: https://umbrellacreators.com/blog/roblox-youtube-video-data-study-2026
- Full list by channel: https://umbrellacreators.com/portfolio

## 3. `duration-2026/` — Length, views and cadence of 1,163 client videos (YouTube Data API)

Every video on Kevin's YT Jobs profile except the main dakblake channel (46 channels), re-read from the YouTube Data API on 2026-10-13: exact duration, views, likes, comments and category.

- 1,159 long-form videos (4 Shorts of 180 s or less are flagged). Median length **12.1 min**; **98.0 %** are 8:00 or longer (mid-roll eligible).
- Within the same channel (7 channels with 20+ videos older than 90 days), 10–20 minute videos had a median of **1.05x** their channel's typical views versus **0.78x** for 8–10 minute videos. This is a correlation, not a cause: topic, title, thumbnail and timing matter too.
- Method, exclusions and controls: views of videos younger than 90 days are excluded from view medians; the API returned 1,164 of 1,164 requested ids; Roodolf's 99 Nights video (XwhPgaPtTi0) reads 26.27 min as a control.
- Used in: https://umbrellacreators.com/answers/my-youtube-retention-is-low-should-i-hire-an-editor

`duration-2026/videos.csv`: video_id, channel, published, title, duration_min, duration_bucket (<8, 8-10, 10-20, 20-35, 35+), views_2026_10_13, likes, comments, format (rule-based on the title: full_movie, rivals_news, dress_to_impress, 99_nights, horror, challenge_obby, rivals_other, other), game_in_title, gaming_channel, is_short_le_180s, age_days, in_views_base (long, 90+ days old, public stats), youtube_category_id.

## Columns

`loudness-2026/videos.csv`: channel, handle, subscribers, video_id, title, published (YYYYMMDD), views, duration_min, integrated_lufs, true_peak_dbtp, words_per_minute.

`roblox-long-form-2026/videos.csv`: channel, video_url, title, published, niche (keyword-based), views_on_2026_10_02, title_length, has_caps_word (a word of 4+ capital letters), has_ellipsis (".."), has_number, has_emoji.

## License

Data: CC BY 4.0. Please credit "Kevin Tabares, Umbrella Creators" and link to https://umbrellacreators.com.
