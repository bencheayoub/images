# Images


## step 1:
First we donwnlaod the images `1.png` and `2.png`.

## step 2:

We see it some pixels manipulation done. So, I wrote a code python.py to get the flag.

```python
from PIL import Image

i1 = Image.open("1.png")
i2 = Image.open("2.png")

pixels = 512

pix1 = i1.load()
pix2 = i2.load()

for i in range(pixels):
	for j in range(pixels):
		if pix1[i,j] == pix2[i,j]:
			pix1[i,j] = 0
		else:
			pix1[i,j] = 255
		
i1.save("flag.png")
```

## Step 3:

after running the code we get the image:

![Image](https://github.com/user-attachments/assets/1074d7dc-2bfc-4b5e-98c0-e3a7d59fb9e5)

## step 4:

Finally, the flag becomes: CTF{I_L0V3_PYTH0N}
