# Lyrics Tags Generator ([tags.notnick.io](https://tags.notnick.io/))

This is a small utility tool for personal use, but you can use it if you have a music/lyric channel on [YouTube](https://www.youtube.com).

## What to provide

| Params     | Required | Description / Options |
|-----------|----------|------------------------|
| `Artist`  | ✅ Yes   | Name of the artist. |
| `Title`   | ❌ No    | Name of the song. |
| `Features`| ❌ No    | Featured artists (3 supported). |
| `TikTok`  | ❌ No    | Boolean flag (`true` / `false`). |
| `Channel` | ❌ No    | Name of the YouTube channel. |
| `Format`  | ❌ No    | • `Lyrics` *(default)*<br>• `Bass Boosted`<br>• `Nightcore/Sped Up`<br>• `Slowed/Reverb`<br>• `Letra`<br>• `Phonk` |
| `Shuffle` | ❌ No    | Shuffle tags option (API only). |
| `Genre`   | ❌ No    | • `None` *(default)*<br>• `Country`<br>• `Latin`<br>• `Phonk`<br>• `Pop`<br>• `Rap` |
| `Verse`   | ❌ No    | Up to 3 short verses. |

If you provide both `artist` and `title` in the `artist` field, you can leave all the other fields empty.

> The `shuffle` option can only be passed in as a query in the API request endpoint. On the site, there's a button that lets you shuffle your tags, and the [bot version](https://discord.com/oauth2/authorize?client_id=1338567480834265193&permissions=2147534848&integration_type=0&scope=bot) shuffles the tags automatically.

Example:

<img width="550" src="https://github.com/user-attachments/assets/84efdc6d-c556-4299-946b-4e2838edb5d5" />

You can also provide the `format` and it will generate the appropriate tags.

The format will _always_ default to `Lyrics` if it isn't provided.

<img width="550" src="https://github.com/user-attachments/assets/b52492a9-7d63-45e1-b5ef-8f0270110b99" />

If the format is provided in both the `artist` and `format` fields, then the format in the `format` field will override the format provided in the `artist` field.

### Important
- The [bot](https://discord.com/oauth2/authorize?client_id=1338567480834265193&permissions=2147534848&integration_type=0&scope=bot) version shuffles tags automatically.
- If you have multiple features, only the first 3 features will be included in the tags.
- You can only provide 3 verses.
- You cannot include numbers or special characters in the `verse` field.
- If the artist, title or even format is included in the `artist` field, then the character limit is 100.
- The character limit for the `artist`, `features` and `channel` fields is 30.
- Character limit for `title` is 45.
- You cannot include special characters in the `artist` field.
- You cannot include commas in the `title` field.

## Data

[Click here to open the json representation.](https://tags.notnick.io/api/generate?title=Residuals&artist=Chris%20Brown&features=none&tiktok=false&format=lyrics&channel=none)

```json
{
    "success": true,
    "tags": "chris brown residuals,chris brown residuals lyrics,residuals lyrics,residuals chris brown lyrics,lyrics residuals,lyrics chris brown residuals,chris brown lyrics residuals,residuals lyric video,lyrics residuals chris brown,chris brown lyrics,lyrics chris brown,residuals,chris brown,residuals chris brown,lyrics",
    "tagsToBeRemoved": [],
    "removedTags": "chris brown residuals,chris brown residuals lyrics,residuals lyrics,residuals chris brown lyrics,lyrics residuals,lyrics chris brown residuals,chris brown lyrics residuals,residuals lyric video,lyrics residuals chris brown,chris brown lyrics,lyrics chris brown,residuals,chris brown,residuals chris brown,lyrics",
    "removedTagsLength": 337,
    "title": "Residuals",
    "artist": "Chris Brown",
    "features": [],
    "hashtags": [
        "ChrisBrown",
        "Residuals",
        "Lyrics"
    ],
    "extras": {},
    "url": "/api/generate?title=Residuals&artist=Chris%20Brown&features=none&tiktok=false&format=lyrics&channel=none&shuffle=false&genre=none&verse=none",
    "length": 337
}
```

## Discord Bot

Using the [Discord](https://discord.com/) bot version is probably faster. You must also be familiar with [slash commands](https://support-apps.discord.com/hc/en-us/articles/26501837786775-Slash-Commands-FAQ).

[Click here to invite the discord bot to your server.](https://discord.com/oauth2/authorize?client_id=1338567480834265193&permissions=2147534848&integration_type=0&scope=bot)

All requests are logged for debugging purposes.

Please [email](mailto:hi@notnick.io) me if you find any bugs.

## Stack

- [Next.js](https://nextjs.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [React.js](https://react.dev/)
- [TailwindCSS](https://tailwindcss.com/)

## License

MIT License

Copyright (c) 2025 Nicholas Njoki

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
