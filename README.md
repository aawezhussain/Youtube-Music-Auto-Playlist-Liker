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

# Use this method at your own risk! Your account can be suspended due to "fake engagement" for automating likes. I’ve successfully liked over 750 song as of 21 Sep, 2024.

# Instructions:
Open the playlist you want to like in your browser (Chrome or another Chromium-based browser is recommended).
Press Ctrl + Shift + J to open the Developer Console.
If pasting isn’t enabled in the console, type allow pasting and press Enter to enable it.
Copy the text from youtube music auto playlist liker.js and paste it into the console, then press Enter.
Avoid manually scrolling the YouTube Music page while the script is running, as it may interfere with the process. It will take some time to complete, so you can minimize the tab and do other things in the meantime.



