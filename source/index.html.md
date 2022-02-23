---
title: rest-quarkus_example API v1.0.0-SNAPSHOT
language_tabs:
  - java: Java
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="rest-quarkus_example-api">rest-quarkus_example API v1.0.0-SNAPSHOT</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

<h1 id="rest-quarkus_example-api-movies">Movies</h1>

This package is created to manage all the movies stored in the database,
  here we can find 2 classes; Movie and MovieResources, where are all the
 endpoints linked to the following methods:
 *  getMovies
 *  countMovies
 *  createMovies
 *  getMovieAuthorById
 *  updateMovie
 *  deleteMovie

## get__movies

`GET /movies`

*getMovies*

 Return all the data about the movies that exists

<h3 id="get__movies-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The return is ok|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something went wrong (BAD_REQUEST)|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|The path was incorrect|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__movies

`POST /movies`

*createMovies*

Add a movie including title, id, and author

> Body parameter

```json
{
  "type": "object",
  "properties": {
    "id": {
      "format": "int64",
      "type": "integer"
    },
    "title": {
      "type": "string"
    },
    "author": {
      "type": "string"
    },
    "duration": {
      "format": "int32",
      "type": "integer"
    }
  }
}
```

<h3 id="post__movies-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Movie](#schemamovie)|false|none|

<h3 id="post__movies-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The movie is added correctly|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something went wrong (BAD_REQUEST)|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|The path was incorrect|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__movies_author_{id}

`GET /movies/author/{id}`

*getMovieAuthorById*

Returns a movie knowing the id of the author

<h3 id="get__movies_author_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|none|

> Example responses

> 200 Response

```json
{
  "type": "object"
}
```

<h3 id="get__movies_author_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The return is ok|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something went wrong (BAD_REQUEST)|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|The path was incorrect|None|

<h3 id="get__movies_author_{id}-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

## get__movies_size

`GET /movies/size`

*countMovies*

 Return  the number of movies that exists

> Example responses

> 200 Response

```json
{
  "format": "int32",
  "type": "integer"
}
```

<h3 id="get__movies_size-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The return is ok|integer|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something went wrong (BAD_REQUEST)|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|The path was incorrect|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__movies_{id}

`DELETE /movies/{id}`

*deleteSong*

Deletes  a movie from the DB knowing the id of the movie

<h3 id="delete__movies_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|none|

<h3 id="delete__movies_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The movie was removed correctly|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something went wrong (BAD_REQUEST)|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|The path was incorrect|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__movies_{id}_{title}

`PUT /movies/{id}/{title}`

*updateMovie*

Updates the title of a movie

<h3 id="put__movies_{id}_{title}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|none|
|title|path|string|true|none|

<h3 id="put__movies_{id}_{title}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The title was updated correctly|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something went wrong (BAD_REQUEST)|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|The path was incorrect|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="rest-quarkus_example-api-songs">Songs</h1>

This package is created to manage all the songs stored in the database,
  here we can find 2 classes; Songs and SongResources, where are all the
  endpoints linked to the following methods:
  - getSongs 
  - countSongs
  - createSongs
  - totalDurationSongs
  - updateGroupSongs
  - deleteSong

## get__songs

`GET /songs`

*getSongs*

 Return all the data about the songs that exists

<h3 id="get__songs-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The return is ok|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something went wrong (BAD_REQUEST)|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|The path was incorrect|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__songs

`POST /songs`

*createSong*

Add a song including name, id, duration and group which belongs

> Body parameter

```json
{
  "type": "object",
  "properties": {
    "id": {
      "format": "int32",
      "type": "integer"
    },
    "name": {
      "type": "string"
    },
    "group": {
      "type": "string"
    },
    "duration": {
      "format": "int64",
      "type": "integer"
    }
  }
}
```

<h3 id="post__songs-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Song](#schemasong)|false|none|

<h3 id="post__songs-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The song is added correctly|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something went wrong|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|The path was incorrect|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__songs_delete_{id}

`DELETE /songs/delete/{id}`

*deleteSong*

Deletes  a song from the DB knowing the id of the song

<h3 id="delete__songs_delete_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|

<h3 id="delete__songs_delete_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The song was removed correctly|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something went wrong (BAD_REQUEST)|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|The path was incorrect|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__songs_modifyGroup_{id}_{newGroupName}

`PUT /songs/modifyGroup/{id}/{newGroupName}`

*updateGroupSong*

Updates the group of a song knowing the ID of the song

<h3 id="put__songs_modifygroup_{id}_{newgroupname}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|
|newGroupName|path|string|true|none|

<h3 id="put__songs_modifygroup_{id}_{newgroupname}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The group was modified correctly|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something went wrong (BAD_REQUEST)|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|The path was incorrect|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__songs_size

`GET /songs/size`

*countSongs*

 Return  the number of songs that exists

> Example responses

> 200 Response

```json
{
  "format": "int32",
  "type": "integer"
}
```

<h3 id="get__songs_size-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The return is ok|integer|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something went wrong (BAD_REQUEST)|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|The path was incorrect|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__songs_totalDuration_{group}

`GET /songs/totalDuration/{group}`

*totalDurationSongs*

Return the time (in minutes) of the total duration of songs that belongs to that group 

<h3 id="get__songs_totalduration_{group}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|group|path|string|true|none|

<h3 id="get__songs_totalduration_{group}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The group was modified correctly|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something went wrong (BAD_REQUEST)|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|The path was incorrect|None|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_Movie">Movie</h2>
<!-- backwards compatibility -->
<a id="schemamovie"></a>
<a id="schema_Movie"></a>
<a id="tocSmovie"></a>
<a id="tocsmovie"></a>

```json
{
  "type": "object",
  "properties": {
    "id": {
      "format": "int64",
      "type": "integer"
    },
    "title": {
      "type": "string"
    },
    "author": {
      "type": "string"
    },
    "duration": {
      "format": "int32",
      "type": "integer"
    }
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|title|string|false|none|none|
|author|string|false|none|none|
|duration|integer(int32)|false|none|none|

<h2 id="tocS_Song">Song</h2>
<!-- backwards compatibility -->
<a id="schemasong"></a>
<a id="schema_Song"></a>
<a id="tocSsong"></a>
<a id="tocssong"></a>

```json
{
  "type": "object",
  "properties": {
    "id": {
      "format": "int32",
      "type": "integer"
    },
    "name": {
      "type": "string"
    },
    "group": {
      "type": "string"
    },
    "duration": {
      "format": "int64",
      "type": "integer"
    }
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|name|string|false|none|none|
|group|string|false|none|none|
|duration|integer(int64)|false|none|none|

