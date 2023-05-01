# Music Store (API)

A test project for Laravel interview. The project is a music store API for managing artists, albums and songs.

## Specifications

### Endpoints

#### `POST /api/auth/register`

Registers a new user.

#### `POST /api/auth/login`

Logs in a user. Returns an access token.

#### `POST /api/albums`

Creates a new album.

##### Authentication

Authentication required.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `title` | String | The album title. |
| `artwork_url` | String | The album artwork URL. |

#### `POST /api/songs`

Creates a new song.

##### Authentication

Authentication required.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `title` | String | The song title. |
| `duration` | Integer | The song duration in seconds. |
| `artist_id` | Integer | The artist ID. |
| `album_id` | Integer | The album ID. (optional) |

#### `GET /api/artists`

Returns a list of artists.

##### Authentication

No authentication required.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `page` | Integer | The page number to return. |
| `limit` | Integer | The number of items to return per page. |

<br>

#### `GET /api/artists/{id}`

Returns a single artist with artist songs and albums.

##### Authentication

No authentication required.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `id` | Integer | The artist ID. |

<br>

#### `POST /api/artists`

Creates a new artist.

##### Authentication

Authentication required.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `name` | String | The artist name. |
| `bio` | String | The artist bio. |
| `avatar` | File | The image. |

<br>

#### `GET /api/songs`

Returns a list of songs.

##### Authentication

No authentication required.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `page` | Integer | The page number to return. |
| `limit` | Integer | The number of items to return per page. |

<br>

#### `GET /api/songs/{id}`

Returns a single song with artist and album.

##### Authentication

No authentication required.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `id` | Integer | The song ID. |
