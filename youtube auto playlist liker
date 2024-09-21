// Function to like all visible songs in the playlist
function likeAllSongs() {
    // Select all the "Like" buttons (not "Liked" ones)
    const likeButtons = document.querySelectorAll('tp-yt-paper-icon-button[aria-label="Like"]');

    if (likeButtons.length === 0) {
        console.log('No more songs to like.');
        return;
    }

    likeButtons.forEach((button, index) => {
        setTimeout(() => {
            // Ensure we are only clicking unliked songs
            if (button.getAttribute('aria-pressed') === 'false') {
                button.click();
                console.log(`Liked song ${index + 1}`);
            }
        }, index * 1000); // Delay to avoid overwhelming the page
    });
}

// Scroll and Like all songs until there are no more unliked songs
function scrollAndLike() {
    let interval = setInterval(() => {
        likeAllSongs();

        // Scroll to the bottom of the page to load more songs if available
        window.scrollBy(0, 1000);

        // Stop the interval when there's no more content to scroll or like
        if (document.querySelectorAll('tp-yt-paper-icon-button[aria-label="Like"]').length === 0) {
            clearInterval(interval);
            console.log('All songs liked.');
        }
    }, 5000); // Delay for scrolling and loading more songs
}

scrollAndLike();
