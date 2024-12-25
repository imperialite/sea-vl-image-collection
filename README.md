
# Image Bulk Submission Guide

If you have many images to contribute to SEAVL, you are welcome to refer to this guide for bulk upload to the [SEA-VL image collection Github Repo](https://github.com/SEACrowd/sea-vl-image-collection ).

## Steps

1. Upload the images to the `data` folder in this [repo](https://github.com/SEACrowd/sea-vl-image-collection).
	 - ⚠️ Please follow the current naming convention, each photo file should be named as `{file_name} - {your_name}.{extension}`.

	 - ⚠️ Keep the maximum image width/height to 2000px, so you might need to resize some images, you can use the following code to resize the image.
		```
		from PIL import Image
		image = Image.open(input_path)
		(w, h) = image.size
		if w > 2000 or h > 2000:
		    if w > h:
		        h = int(h * 2000. / w) 
		        w = 2000 
		    else:
		        w = int(w * 2000. / h)
		        h = 2000
		image = image.resize((w, h), Image.BILINEAR) 
		image.save(output_path)
		```
2. Use the CSV sample ([link](https://www.dropbox.com/scl/fi/xiae0op7nj58ajt1l2yky/seavl_bulk_upload_format.csv?rlkey=izd3c28vy0b35grc1utykoxsk&dl=0)) to provide more details on the submitted photos. 
	- ⚠️ Keep the empty column as empty.
	- ⚠️ For the `email` column just fill it with seacrowd.research@gmail.com.
	- ⚠️ For the `image` column, please fill it with `https://raw.githubusercontent.com/SEACrowd/sea-vl-image-collection/refs/heads/main/data/%7Bfile_name%7D`. `file_name` should be the same as the one you submitted to the repository.
3.  As the last step, you can send us the CSV through Discord / email (contact.ruochen@gmail.com or samuel.cahyawijaya@gmail.com) and we will review the CSV and images. If there is no issue, we will push the photos to the annotation platform.

**Any questions?** Message `@rc.z` or `@samuelcahyawijaya` on [Discord](https://discord.gg/URdhUGsBUQ)!
