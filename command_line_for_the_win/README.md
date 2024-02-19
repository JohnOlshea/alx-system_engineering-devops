# Project README

## Uploading Screenshots to Sandbox Environment and Pushing to GitHub

This guide outlines the steps to upload screenshots to a sandbox environment using SFTP command-line tool and then push them to GitHub.

### Prerequisites

- Access to the sandbox environment (hostname, username, and password).
- SFTP command-line tool installed on your local machine.

### Steps

1. **Take Screenshots**: Complete the levels as mentioned in the general requirements and take screenshots of the completed levels.

2. **Open Terminal or Command Prompt**: Open a terminal or command prompt on your local machine.

3. **Establish Connection to Sandbox Environment**: Use the SFTP command-line tool to establish a connection to the sandbox environment. Replace `hostname`, `username`, and `password` with your actual sandbox environment credentials:

    ```bash
    sftp username@hostname
    ```

4. **Navigate to Directory**: Once connected, navigate to the directory where you want to upload the screenshots. For example, if you want to upload to a directory named `screenshots`, use:

    ```bash
    cd screenshots
    ```

5. **Upload Screenshots**: Use the `put` command to upload the screenshots from your local machine to the sandbox environment. Replace `local_file_path` with the actual path to your screenshots:

    ```bash
    put local_file_path
    ```

6. **Confirm Transfer**: Confirm that the screenshots have been successfully transferred by checking the sandbox directory.

7. **Push to GitHub**: Once the screenshots are transferred, you can proceed to push the screenshots to GitHub as mentioned in the initial requirements.

### Example

Here's an example command sequence for uploading a screenshot named `level1.png` to a sandbox directory named `screenshots`:

```bash
sftp username@hostname
cd screenshots
put /path/to/level1.png
