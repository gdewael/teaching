# teaching
Collection of stuff done for teaching at bw26

A lot of my teaching stuffs are also now located on the [MLLS course GitHub](https://github.com/bioml-ugent/MLLS).

### Notes to self:
- Jupyter notebooks on GitHub can be linked to colab and shared with students without having to upload to Drive. In colab: "Open > GitHub" and copy link.
- Uploading the data to GitHub and using `urllib` to download them ensures that all students seamlessly access the data without having to download separate files and will work on all platforms (unlike using `!wget`). Example:

```python
import urllib.request
urllib.request.urlretrieve("datafile_url", "downloaded_file_location")
```

- Like-wise, embedding images from the net is best practise: `<img src="link" width = x>`.