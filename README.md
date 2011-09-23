# Facebook Photo Downloader
Download all of the photos in any Facebook album that you have permission to view

## Instructions

1) Copy the [bookmarklet js](https://raw.github.com/evanbeard/Facebook-Photo-Downloader/master/bookmarklet.js) 
into a bookmark (go to bookmarks -> bookmark manager, or equivalent, and copy-paste all of the code into
the box as if you were making a bookmark for, e.g., google.com.
2) Go to any photo in the album you want to download. The url should look like
this "https://www.facebook.com/photo.php?fbid=8532030814&set=a.665432525484.2233540.1310135&type=1".
You don't want to be in the theatre (remove "&theatre" from the url to get out of it).
3) Run the bookmarklet
4) Follow instructions printed to the javascript console (you'll use wget to download your images)   


## FAQ

- How does it work?   
This application directs your browser to visit each photo in an album and collects the download URLs,
then puts the urls in a format that wget can use to download all of the photos. It shouldn't be
blocked by facebook because it looks just like you do when navigating between photos.

- Why can't I use a tool such as PhotoGrabber to do this?   
Many people set their privacy settings so that third party applications cannot access their albums,
so third party apps such as PhotoGrabber will not download all photos available to you.

- Why can't I use Facebook's tool to download my own data   
You can, but this only allows you to download your own albums, not those that belong to others.

- Why do we need to use wget to download the images?   
On older facebook photos the images do not always send download headers, so a window.location will not download the
image but instead redirect the entire window. So we collect the image links and let wget do the downloading.

## Disclaimer
- use at your own risk.
- only tested on Chrome but should work in any modern browser
