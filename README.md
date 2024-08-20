# Vamp-Hanime-Scraper
Vamp Hanime Scraper

Vamp Hanime Scraper is a Node.js library designed to scrape metadata, descriptions, thumbnails, download links, and tags from Hanime.tv. This scraper is perfect for developers who need to programmatically extract data from Hanime.tv for use in their applications.

Features

	•	Fetch Metadata: Retrieve detailed information about a video, such as brand, release date, upload date, view count, and more.
	•	Extract Descriptions: Get the full description of the video content.
	•	Download Thumbnails: Extract the URL for the video’s thumbnail.
	•	Get Download Links: Obtain direct download links for the video.
	•	Retrieve Tags: Fetch all tags associated with the video.

Installation

You can easily install the Vamp Hanime Scraper via npm. Make sure you have Node.js installed on your system.

Step 1: Install via npm

npm install vamp-hanime-scraper

Step 2: Import the Library

const { getInfo, getDescription, getThumbnail, getDownloadUrl, getTags } = require('vamp-hanime-scraper');

Usage

Here’s a quick guide on how to use the Vamp Hanime Scraper to fetch various data points from a Hanime.tv video page.

Example Usage

const { getInfo, getDescription, getThumbnail, getDownloadUrl, getTags } = require('vamp-hanime-scraper');

const url = 'https://hanime.tv/videos/hentai/sample-video';

(async () => {
    try {
        const info = await getInfo(url);
        const description = await getDescription(url);
        const thumbnail = await getThumbnail(url);
        const downloadUrl = await getDownloadUrl(url);
        const tags = await getTags(url);

        console.log({ info, description, thumbnail, downloadUrl, tags });
    } catch (error) {
        console.error('Error fetching data:', error);
    }
})();

API Methods

	1.	getInfo(url: string) -> Promise
Fetches the metadata of the video.
	2.	getDescription(url: string) -> Promise
Fetches the description of the video.
	3.	getThumbnail(url: string) -> Promise
Fetches the thumbnail URL of the video.
	4.	getDownloadUrl(url: string) -> Promise
Fetches the download URL of the video.
	5.	getTags(url: string) -> Promise<string[]>
Fetches the tags associated with the video.

Sample Output

Here is an example of what the output might look like:

{
  "info": {
    "brand": "Example Brand",
    "branduploads": "5",
    "releasedate": "January 1, 2020",
    "uploaddate": "January 2, 2020",
    "views": "100,000 views",
    "censored": true,
    "alternatetitles": ["Title1", "Title2"]
  },
  "description": "This is the description of the video.",
  "thumbnail": "https://example.com/thumbnail.jpg",
  "downloadUrl": "https://hanime.tv/downloads/encodedurl",
  "tags": ["tag1", "tag2", "tag3"]
}

How to Contribute

Contributions are welcome! If you have ideas, requests, or bug reports, feel free to open an issue or submit a pull request.

	1.	Fork the Repository
	2.	Create a New Branch: git checkout -b feature/my-new-feature
	3.	Commit Your Changes: git commit -am 'Add some feature'
	4.	Push to the Branch: git push origin feature/my-new-feature
	5.	Submit a Pull Request

License

This project is licensed under the MIT License - see the LICENSE file for details.

Disclaimer

This tool is intended for educational purposes only. Please respect the terms of service of any site you scrape.
