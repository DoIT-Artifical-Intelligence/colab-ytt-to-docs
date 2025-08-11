# Colab YouTube Transcription Extractor

Extract YouTube video transcripts and save them directly to Google Docs using Google Colab.

## Features
- Fetches YouTube video transcripts using the [youtube-transcript-api](https://github.com/jdepoix/youtube-transcript-api)
- Saves the transcript to a new Google Doc in your Google Drive

## How to Use in Google Colab

1. **Open Google Colab**
	- Go to [Google Colab](https://colab.research.google.com/).
2. **Upload the Notebook**
	- Download `Colab_YouTube_Transcription_Extractor.ipynb` from this repository.
	- In Colab, click `File > Upload notebook` and select the file.
3. **Set the YouTube URL and API Key**
	 - In the first cell, replace the sample URL and title fallback with details for your target YouTube video link:
		 ```python
		 YOUTUBE_URL = "https://www.youtube.com/watch?v=XXXXXXXXXXX"
         VIDEO_TITLE_FALLBACK = "INSERT VIDEO NAME"
		 ```
	 - Add your YouTube Data API key to Colab secrets:
		 - In Colab, go to `Runtime > Manage secrets` and add a new secret named `YOUTUBE_DATA_API_KEY` with your API key value.
         - Check the "Notebook access" toggle.
	 - To register for a YouTube Data API key:
		 1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
		 2. Create a new project (or select an existing one).
		 3. Enable the YouTube Data API v3 for your project.
		 4. Go to `APIs & Services > Credentials` and create an API key.
		 5. Copy the API key and add it to Colab secrets as described above.
4. **Run All Cells**
	- Click `Runtime > Run all` to execute the notebook.
	- Authenticate with your Google account when prompted.
	- Provide your YouTube Data API key if required.
	- **Note:** The notebook will ask for access to your Google Drive in order to create the transcript file. You must grant access to proceed.
5. **Get the Transcript**
	- The notebook will fetch the transcript and create a new Google Doc in your Drive.
	- A shareable link to the document will be printed at the end.

## Requirements
- Google Colab
- YouTube Data API key (for fetching video title)
- Access to Google Drive

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
