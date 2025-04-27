# 📌 Jellyfin Icon Metadata

## 🔥 Description

Enhance your Jellyfin experience by replacing text-based metadata provider links with icons. This plugin supports various metadata providers across different media types.

### Supported Providers

#### Movies/TV Shows/Anime/Music

- anilist.co
- anidb.net
- anisearch.com
- bgm.tv
- hikka.io
- movie.douban.com
- imdb.com
- kitsu.app
- myanimelist.net
- shikimori.one
- Shoko (local metadata provider)
- Stash (local metadata provider)
- themoviedb.org
- themoviedb.org/collection
- theporndb.net
- thetvdb.com
- trakt.tv
- tvmaze.com
- kinopoisk.ru
- tvlistings.zap2it.com

#### Books/Comics/Manga

- comicvine.gamespot.com
- books.google.com
- search.worldcat.org
- hikka.io

#### Music

- music.apple.com
- discogs.com
- musicbrainz.org
- theaudiodb.com
- vgmdb.net
- imvdb.com

## Adding New Metadata Providers

To add a new metadata provider, simply provide a link to the plugin that integrates the metadata provider.

## Installation

### Public Metadata Providers

Most icons can be imported using the following CSS:

```css
@import url("https://cdn.jsdelivr.net/gh/Druidblack/jellyfin-icon-metadata@main/public-icon.css");
```

Add this to the top of `Dashboard -> General -> Custom CSS code`.

### Local Metadata Providers

For local metadata providers like Stash and Shoko, update the CSS files with your local server address.

#### Shoko

Modify and add the following CSS to the top of `Dashboard -> General -> Custom CSS code`:

```css
.itemExternalLinks a[href*="http://CHANGE_ME:8111/webui/collection/group"] {
    background: none !important;
    color: transparent !important;
    padding: 0 !important;
}

.itemExternalLinks a[href*="http://CHANGE_ME:8111/webui/collection/group"]::before {
	content: "";
	display: inline-block;
	width: 60px;
	height: 25px;
	background-image: url('https://cdn.jsdelivr.net/gh/Druidblack/jellyfin-icon-metadata@main/icons/shoko/shoko-group.png');
	background-size: contain;
	background-repeat: no-repeat;
	margin-right: 5px;
	vertical-align: middle;
}

.itemExternalLinks.focuscontainer-x > a[href*="http://CHANGE_ME:8111/webui/collection/group"]:hover,
.itemExternalLinks.focuscontainer-x > a[href*="http://CHANGE_ME:8111/webui/collection/group"]:focus,
.itemExternalLinks.focuscontainer-x > a[href*="http://CHANGE_ME:8111/webui/collection/group"]:active {
    background: none !important;
    filter: none !important;
    border: none !important;
}

.itemExternalLinks a[href*="http://CHANGE_ME:8111/webui/collection/group"] {
	font-size: 0;
}

.itemExternalLinks a[href*="http://CHANGE_ME:8111/webui/collection/series"] {
    background: none !important;
    color: transparent !important;
    padding: 0 !important;
}

.itemExternalLinks a[href*="http://CHANGE_ME:8111/webui/collection/series"]::before {
	content: "";
	display: inline-block;
	width: 60px;
	height: 25px;
	background-image: url('https://cdn.jsdelivr.net/gh/Druidblack/jellyfin-icon-metadata@main/icons/shoko/shoko-series.png');
	background-size: contain;
	background-repeat: no-repeat;
	margin-right: 5px;
	vertical-align: middle;
}

.itemExternalLinks.focuscontainer-x > a[href*="http://CHANGE_ME:8111/webui/collection/series"]:hover,
.itemExternalLinks.focuscontainer-x > a[href*="http://CHANGE_ME:8111/webui/collection/series"]:focus,
.itemExternalLinks.focuscontainer-x > a[href*="http://CHANGE_ME:8111/webui/collection/series"]:active {
    background: none !important;
    filter: none !important;
    border: none !important;
}

.itemExternalLinks a[href*="http://CHANGE_ME:8111/webui/collection/series"] {
	font-size: 0;
}

.itemExternalLinks a[href*="http://CHANGE_ME:8111/webui/redirect/episode"] {
    background: none !important;
    color: transparent !important;
    padding: 0 !important;
}

.itemExternalLinks a[href*="http://CHANGE_ME:8111/webui/redirect/episode"]::before {
	content: "";
	display: inline-block;
	width: 65px;
	height: 25px;
	background-image: url('https://cdn.jsdelivr.net/gh/Druidblack/jellyfin-icon-metadata@main/icons/shoko/shoko-episode.png');
	background-size: contain;
	background-repeat: no-repeat;
	margin-right: 5px;
	vertical-align: middle;
}

.itemExternalLinks.focuscontainer-x > a[href*="http://CHANGE_ME:8111/webui/redirect/episode"]:hover,
.itemExternalLinks.focuscontainer-x > a[href*="http://CHANGE_ME:8111/webui/redirect/episode"]:focus,
.itemExternalLinks.focuscontainer-x > a[href*="http://CHANGE_ME:8111/webui/redirect/episode"]:active {
    background: none !important;
    filter: none !important;
    border: none !important;
}

.itemExternalLinks a[href*="http://CHANGE_ME:8111/webui/redirect/episode"] {
	font-size: 0;
}

.itemExternalLinks a[href*="http://CHANGE_ME:8111/webui/redirect/file"] {
    background: none !important;
    color: transparent !important;
    padding: 0 !important;
}

.itemExternalLinks a[href*="http://CHANGE_ME:8111/webui/redirect/file"]::before {
	content: "";
	display: inline-block;
	width: 60px;
	height: 25px;
	background-image: url('https://cdn.jsdelivr.net/gh/Druidblack/jellyfin-icon-metadata@main/icons/shoko/shoko-file.png');
	background-size: contain;
	background-repeat: no-repeat;
	margin-right: 5px;
	vertical-align: middle;
}

.itemExternalLinks.focuscontainer-x > a[href*="http://CHANGE_ME:8111/webui/redirect/file"]:hover,
.itemExternalLinks.focuscontainer-x > a[href*="http://CHANGE_ME:8111/webui/redirect/file"]:focus,
.itemExternalLinks.focuscontainer-x > a[href*="http://CHANGE_ME:8111/webui/redirect/file"]:active {
    background: none !important;
    filter: none !important;
    border: none !important;
}

.itemExternalLinks a[href*="http://CHANGE_ME:8111/webui/redirect/file"] {
	font-size: 0;
}
```

#### Stash

Modify and add the following CSS to the top of `Dashboard -> General -> Custom CSS code`:

```css
.itemExternalLinks a[href*="http://CHANGE_ME:9999/scenes"]::before {
	content: "";
	display: inline-block;
	width: 35px;
	height: 25px;
	background-image: url('https://raw.githubusercontent.com/Druidblack/jellyfin-icon-metadata/refs/heads/main/icons/stash/stash.png');
	background-size: contain;
	background-repeat: no-repeat;
	margin-right: 5px;
	vertical-align: middle;
}

.itemExternalLinks a[href*="http://CHANGE_ME:9999/scenes"] {
	font-size: 0;
}
```

## Screenshots
![Movies](https://github.com/user-attachments/assets/b7645f41-bf4a-4929-b14e-1e7b78f8a99a)
![TV Shows](https://github.com/user-attachments/assets/5536574a-1dd7-4412-9a82-7d542476baca)
![Music Artist](https://github.com/user-attachments/assets/7ac06608-90b1-43d9-8c47-9acb5cb293e2)
![Music Album](https://github.com/user-attachments/assets/bbd02b34-59ee-46f4-9326-6f8aa1f18c99)
![Books](https://github.com/user-attachments/assets/2f13825d-5f07-4dea-87b3-e3ab81120c47)
![Anime](https://github.com/Druidblack/jellyfin-icon-metadata/blob/main/image/anime%20menu.jpg)
![Anime Episode](https://github.com/user-attachments/assets/2a04a2f9-ac98-4017-a838-37ca733489eb)

**Credits:** This idea was inspired by the theme [Finimalism](https://github.com/tedhinklater/finimalism).
