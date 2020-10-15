
# Image Carousel - Svelte

Clone repo

```bash
git clone https://github.com/bmw2621/svelte-carousel
```

*Note that you will need to have [Node.js](https://nodejs.org) installed.*


## Get started

Install the dependencies...

```bash
cd svelte-carousel
yarn
```

...then start [Rollup](https://rollupjs.org):

```bash
yarn dev
```

Navigate to [localhost:5000](http://localhost:5000). You should see your app running.

> See tutorial at https://www.youtube.com/watch?v=Ikgw-ybpTtY


## Carousel
 Carousel will expand to the full width of the containing element

### Parameters

| parameter    |  default |                                                                                                                                                                    usage |
|--------------|:--------:|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| images       | REQUIRED | Array of objects.  Each must have a path attribute, with a string representing the path the the image, and an id attribute for the image element represented as a string |
| imageWidth   |    300   |                                                                                                                    Integer representing width of all images in carousel. |
| imageSpacing |    20    |                                                                                                                Integer representing number of pixels between each image. |
| speed        |    500   |                                                                                                      Integer representing number of milliseconds for transition to occur |
| controlColor | '#444'   |                                                                                                    String representing hex value or HTML color to color default controls |
| controlScale | '0.5'    |                                                                                                     String representation of float to determine size of default controls |

### Custom Controls - Slots
Custom controls may be passed in to the respective slots `slot="left-control"` and `slot="right-control"`

Example:
```
import { ChevronLeftIcon, ChevronRightIcon } from 'svelte-feather-icons';

<script>
  const images = [
    {path: 'images/image1.jpg', id: 'image1'},
    {path: 'images/image2.jpg', id: 'image2'},
    {path: 'images/image3.jpg', id: 'image3'},
    {path: 'images/image4.jpg', id: 'image4'},
    {path: 'images/image5.jpg', id: 'image5'}
  ]
</script>

<Carousel {images}>
  <span slot="left-control"><ChevronLeftIcon /></span>
  <span slot="right-control"><ChevronRightIcon /></span>
</Carousel>

```
