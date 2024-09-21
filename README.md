# Youtube-Auto-Playlist-Liker
This JavaScript code automatically likes all unliked songs in a YouTube Music playlist. It checks the "Like" buttons and only clicks those with `aria-pressed="false"`, ensuring it doesn't dislike already liked songs. The script scrolls to load more songs and repeats the process until all songs are liked, then stops automatically.

This JavaScript code automates the process of liking all songs in a YouTube Music playlist without accidentally disliking any that are already liked. Here's a breakdown of how it works:

- Finding "Like" Buttons: The code scans the page for all visible "Like" buttons. These buttons have an aria-label attribute set to "Like", which is used to identify them. 
It filters out songs that are already liked by checking the aria-pressed attribute. If aria-pressed is "false", the song is not yet liked and is safe to like.

- Liking Unliked Songs: For each unliked song, the script clicks the "Like" button with a short delay between actions (1 second per song) to avoid spamming too many clicks at once.

- Auto-Scrolling to Load More Songs: Since YouTube Music playlists often load additional songs when you scroll, the script scrolls down the page after liking the visible songs. This allows more songs to appear.

- Repeating the Process: The script keeps checking for new "Like" buttons as it scrolls. It continues the process of liking visible songs and scrolling until no more songs are left to like or load.

- Stopping Automatically: When there are no more unliked songs, or the playlist is fully loaded, the script stops itself automatically and logs a message indicating that all songs have been liked.

By ensuring that only songs with aria-pressed="false" are clicked, the script avoids disliking any songs that have already been liked.

# Instructions:
Open the playlist you want it to be liked in the browser (chrome or other chromium based recommended), then Press `ctrl + shift + j` to open the Developer Console.
if pasting isn't enable in the console you may **manual** type `allow pasting` to enable the paste the script directly from clipboard.
Then copy the text directy from this file [JavaScript file](Youtube-Music-Auto-Playlist-Liker/youtube music auto playlist liker.js)

