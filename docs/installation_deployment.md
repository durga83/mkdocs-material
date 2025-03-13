# Installation & Deployment

Follow these steps to install and deploy **Smart Recruiter** on your system.

---

## 1. Download the Binary File and Folder Structure

1. Download the **Folder Structure** and **Smart_Recruiting** executable file from a Git repository or a zipped archive.
2. Extract the contents to a directory of your choice.

---

## 2. Copy to Deployment Directory

1. Place the downloaded files in a preferred working directory.
2. Ensure the folder structure is intact after extraction.

---

## 3. Configure Dependencies

### .env File
The `.env` file contains environment variables that configure the application. Follow these steps to set it up:

1. Open the `.env` file in a text editor.
2. Modify the following variables according to your setup:

| Variable               | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| `GEMINI_API_KEY`       | Enter your Google Gemini API key.                                           |
| `GEMINI_MODEL_NAME`    | The model is set to `gemini-1.5-flash`. You probably don't have to change this. |
| `BASE_JD_DIR`          | Specify the directory where your Job Description (JD) files are located.    |
| `SUMMARY_OUTPUT_FILE`  | Specify the file path where the results will be saved.                      |
| `JSON_INPUT_DIR`       | This is a temporary directory for JSON input files.                         |
| `TEMPLATE_DIR`         | Specify the directory where the resume templates are located.               |
| `LOGO_PATH`            | Specify the path where the company logo is located.                         |
| `INPUT__LLM_PROMPT`    | Specify the prompt file name (without the extension) for the Gemini model. For example, `gemini_1` or `gemini_2`. Ensure the prompt files are located in the correct directory. |
| `OUTPUT__RESUME_FORMAT`| Specify the desired resume output formats (comma-separated): `docx,html,md,pdf`. |
| `USERNAME`             | Enter your username for license validation.                                 |
| `EMAIL`                | Enter your email for license validation.                                    |
| `SECRET_KEY`           | **Do not modify manually.** This key is automatically generated during the license generation step. |
| `LICENSE_KEY`          | **Do not modify manually.** This key is automatically generated during the license generation step. |
| `TESSERACT_MODE`       | Choose `ON` if you want to parse only `.pdf` formats in your JD directories with the help of `TESSERACT_CMD`. Choose `OFF` if you want to parse both `.pdf` and `.docx` formats and use the file data directly without `TESSERACT_CMD`. |

---

## 4. Verify Configuration

After editing the `.env` file, verify that all variables are correctly configured. Ensure the paths and keys are accurate.
