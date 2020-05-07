# google-colab

## To save file in google drive
To save a file in google drive, we need to mount google drive to our Colab session.

```python
from google.colab import drive
drive.mount('/content/gdrive')
```
Google-colab will now ask for your authorization code (they will provide a link).
Enter the your authorization code and you are ready to begin

Now creating or writing files is simple as
```python
with open('/content/gdrive/My Drive/file_name.txt', 'w') as f:
  f.write('content')
```

__NOTE__: If you are creating/writing a file inside a directory, that directory _must_ exist in the google-drive.

## Reading a file from google-drive

```python
with open('/content/gdrive/My Drive/file_name.txt', 'r') as f:
  f.read()
```

## Downloading a file from google-drive
To download a file from google-drive to your local machine
```python
from google.colab import files
files.download("/content/gdrive/My Drive/testfile.txt")
```
