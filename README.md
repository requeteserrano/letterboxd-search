# Letterboxd Advanced Search

A simple client-side interface for building Letterboxd advanced film searches.

The application uses only:

- HTML
- CSS
- JavaScript

Queries are build locally. No framework, backend, database, API key, or build process is required.

## Features

- Add unlimited search filters.
- Include or exclude each filter independently.
- Use the same field multiple times.
- Generates a Letterboxd search URL.
- Button to open the search directly in Letterboxd.
- Responsive layout for desktop and mobile screens.

## Usage

1. Save `index.html` and open it in any modern web browser.

3. Click **Add filter**.

4. Select a field, such as *Actor* or *Director*, choose either **Include** or **Exclude** and enter a value.

7. Repeat for more conditions.

8. Click **Open in Letterboxd**.

## Supported fields

Some filters like *Country* are only available when [exploring the catalogue](https://letterboxd.com/films/country/spain/) 
and not through the search engine, and thus are not offered.

If any valid filter is missing, please let us know.

## How values are formatted

The application converts entered values to lowercase and replaces spaces with hyphens.

For example:

```text
James Cameron
```

becomes:

```text
james-cameron
```

The generated filter is:

```text
producer:james-cameron
```

Excluded values receive a leading hyphen:

```text
-producer:james-cameron
```

## Raw search terms

The **Raw search terms** field can be used for terms that are not represented by one of the predefined filter types.

For example:

```text
black-and-white
```

is appended to the generated query.

## Browser support

The application is intended for modern browsers that support:

- ES6 JavaScript
- `navigator.clipboard`
- CSS Grid
- CSS custom properties

If clipboard permissions are unavailable, the application falls back to selecting and copying the generated query manually.

## Limitations

- The application does not fetch or display Letterboxd search results.
- It does not use the Letterboxd API.
- It does not validate whether a person, genre, country, or service exists.
- Search behavior ultimately depends on Letterboxd’s search syntax and URL handling.
