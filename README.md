
# Affiliate Content Generation Project

## Project Overview

This project is designed to streamline the process of generating granular article topics and content optimized for SEO for affiliate sites. The content generated by the script is stored in a structured HTML format and automatically uploaded to a Google Drive folder, adhering to an internal process for efficient content management and sharing.

The script leverages OpenAI’s language model to generate multiple article ideas based on a provided subject, then outlines and fully drafts each article in an SEO-friendly HTML structure. Each article is saved as a Word document and uploaded to Google Drive for easy access and review.

## How It Works

1. **Title Generation**: Generates a specified number of unique and SEO-relevant article titles based on the main subject.
2. **Detailed Outline**: For each title, a structured outline is created to guide content development, ensuring each article provides professional insights relevant to the topic.
3. **HTML Article Generation**: Follows the outline to generate an article in HTML, formatted for SEO, and includes essential HTML tags (`<h1>`, `<h2>`, `<p>`, `<strong>`, etc.) as specified.
4. **SEO Optimization**: Provides a concise SEO title, description, and URL path for each article.
5. **Upload to Google Drive**: The content is saved in a `.docx` format and uploaded to a Google Drive folder, streamlining the content storage and approval process.

## Configuration and Setup

### Prerequisites

- **OpenAI API Key**: The script requires an OpenAI API key, stored securely in a local text file.
- **Google Drive API Access**: Requires a Google service account JSON file for authentication to access Google Drive.

### Folder Structure

1. **`keys.txt`**: This file should contain your OpenAI API key on the first line. (Ensure this file is created and stored securely.)
2. **Service Account JSON**: The path to the service account JSON file for Google Drive API access should be set in the script under the variable `SERVICE_ACCOUNT_FILE`.

### Variables to Modify

- **`subject`**: The main subject/topic for the articles. Adjust this to align with the affiliate site’s focus.
- **`num_titles`**: The number of unique articles to generate. This can be adjusted based on the scope of the project.
- **`project_name`**: The name of the project, which will serve as the folder name in Google Drive.
- **`drive_folder_id`**: The ID of the parent folder in Google Drive where the generated articles will be stored. This needs to be updated for each new project if the location changes.

### Example Structure for Configuration Files

1. **`keys.txt`**
   ```
   YOUR_OPENAI_API_KEY
   ```

2. **Service Account JSON (`service_account.json`)**
   Download the JSON file from Google Cloud Console and update `SERVICE_ACCOUNT_FILE` in the script to point to this file’s location.

## Usage

1. Place your OpenAI API key in the `keys.txt` file.
2. Update the `SERVICE_ACCOUNT_FILE` variable to point to the Google Drive service account JSON file.
3. Modify `subject`, `num_titles`, `project_name`, and `drive_folder_id` based on your project requirements.
4. Run the script to generate articles, which will be saved in the designated Google Drive folder.

### Running the Script

To run the script, use:

```bash
python your_script_name.py
```

## Important Notes

- **API Key Security**: Keep the `keys.txt` file secure and do not share it. This file should not be included in version control to prevent exposing the API key.
- **Service Account Security**: The service account JSON file contains sensitive credentials for accessing Google Drive. Keep this file secure and avoid exposing it in public repositories.

## Future Customization

- **Scaling Titles and Content Length**: Modify `num_titles` and `min_word_count` to scale the number of articles or adjust content length to fit specific SEO and marketing needs.
- **Content Customization**: The subject and outline generation prompts are designed to be flexible, allowing the script to adapt to a variety of topics and industries.

## License

This project is intended for internal use only and should be adapted responsibly for each affiliate site to ensure unique, value-added content.

---

**End of README**
