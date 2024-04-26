# Clothing-Style-Transfer

Taking an image of clothing and a style image, and blending them together so that the clothing is in the style of the style image.

## Running

set the path to the content image (mask) and style image in the file.

```py
# path to images
CONTENT_IMG_PATH = "path/to/image"
STYLE_IMG_PATH = "path/to/style"

# image will save every epoch under
# save/IMG_SAVE_NAME-{n}.png
IMG_SAVE_NAME = "style_transferred_image"
```

You can alter the weights in the style_weight, content_weight, and total_variation_weight

```py
style_weight = 1e-2  # default: 1e-2
content_weight = 1e4  # default: 1e4
total_variation_weight = 30  # default: 30
```

## Examples

Running for around 10 epochs(1000 steps) tends to yield the best results. With certain images it may be better to run more or less epochs as well as editing the weights to generate a better image. Different weight combinations may work better with more or less epochs.

The following example was run with 10 epochs with default weights.

<img src="./save/cityscape-scream/9.png" alt="Blended Neural Style Image" width="500" />

The Content Image and Style Image for this example

Content Image:

<img src="./images/content/cityscape.jpg" alt="Content Image" width="500" />

Style Image:

<img src="./images/style/scream.jpg" alt="Style Image" width="500" />

### Other Examples

Deepspace Scene style with La Muse Painting

<img src="./save/deepspace-art/deepspace-art-9.png" alt="Deepspace-Art Painting" width="500" />

Sunset mountain style with Greatwave Painting

<img src="./save/sunset-greatwave/sunset-greatwave-8.png" alt="Sunset Mountain Painting" width="500" />

Vertical City Scene styled with Scream Painting

<img src="./save/city-scream/9.png" alt="Cityscape blended painting" width="500" />

## Dependencies

Install dependencies with Pip

`pip install tensorflow numpy Pillow`

Dependencies:

- Tensorflow
- Numpy
- Pillow

## License

[MIT](https://choosealicense.com/licenses/mit/)
