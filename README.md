# Homework №8 `goit-js-hw-08`

## Instructions

Create a repository **`goit-js-hw-08`** and clone it to your computer.  
Inside the `goit-js-hw-08` folder, create the project structure as shown in the diagram below.

![Project preview](assets/goit-js-08.jpg)

> **Attention!** File and folder names, as well as their nesting structure, must match the diagram exactly. Otherwise, your work will not be accepted.

> [!NOTE] To style the markup of your tasks, use this
> [template](https://www.figma.com/file/m8k9NQV7qZrtYDCvxfD68B/%D0%94%D0%97-JavaScript?type=design&node-id=3-941&mode=design).

#### Task — Image Gallery

Create a gallery with clickable items that open the full-size image in a modal window. Check the demo video of the gallery.

## 🎥 Video

https://github.com/user-attachments/assets/dd073bcd-7e57-48df-9ad4-e5218b037bc4

Creating the gallery is a complex task, so it’s better to break it down into smaller subtasks. Completing each subtask brings you closer to the final goal. This process is called task decomposition.

#### 1 – Gallery Markup

It’s logical to start by creating the container where the gallery items will be added.  
In your HTML code, add a gallery container — an unordered list with the class `gallery`.

```js
const images = [
  {
    preview:
      "https://cdn.pixabay.com/photo/2019/05/14/16/43/rchids-4202820__480.jpg",
    original:
      "https://cdn.pixabay.com/photo/2019/05/14/16/43/rchids-4202820_1280.jpg",
    description: "Hokkaido Flower",
  },
  {
    preview:
      "https://cdn.pixabay.com/photo/2019/05/14/22/05/container-4203677__340.jpg",
    original:
      "https://cdn.pixabay.com/photo/2019/05/14/22/05/container-4203677_1280.jpg",
    description: "Container Haulage Freight",
  },
  {
    preview:
      "https://cdn.pixabay.com/photo/2019/05/16/09/47/beach-4206785__340.jpg",
    original:
      "https://cdn.pixabay.com/photo/2019/05/16/09/47/beach-4206785_1280.jpg",
    description: "Aerial Beach View",
  },
  {
    preview:
      "https://cdn.pixabay.com/photo/2016/11/18/16/19/flowers-1835619__340.jpg",
    original:
      "https://cdn.pixabay.com/photo/2016/11/18/16/19/flowers-1835619_1280.jpg",
    description: "Flower Blooms",
  },
  {
    preview:
      "https://cdn.pixabay.com/photo/2018/09/13/10/36/mountains-3674334__340.jpg",
    original:
      "https://cdn.pixabay.com/photo/2018/09/13/10/36/mountains-3674334_1280.jpg",
    description: "Alpine Mountains",
  },
  {
    preview:
      "https://cdn.pixabay.com/photo/2019/05/16/23/04/landscape-4208571__340.jpg",
    original:
      "https://cdn.pixabay.com/photo/2019/05/16/23/04/landscape-4208571_1280.jpg",
    description: "Mountain Lake Sailing",
  },
  {
    preview:
      "https://cdn.pixabay.com/photo/2019/05/17/09/27/the-alps-4209272__340.jpg",
    original:
      "https://cdn.pixabay.com/photo/2019/05/17/09/27/the-alps-4209272_1280.jpg",
    description: "Alpine Spring Meadows",
  },
  {
    preview:
      "https://cdn.pixabay.com/photo/2019/05/16/21/10/landscape-4208255__340.jpg",
    original:
      "https://cdn.pixabay.com/photo/2019/05/16/21/10/landscape-4208255_1280.jpg",
    description: "Nature Landscape",
  },
  {
    preview:
      "https://cdn.pixabay.com/photo/2019/05/17/04/35/lighthouse-4208843__340.jpg",
    original:
      "https://cdn.pixabay.com/photo/2019/05/17/04/35/lighthouse-4208843_1280.jpg",
    description: "Lighthouse Coast Sea",
  },
];
```

#### 3 – Gallery Items Markup

You have a container where gallery items can be added, and you have the data to create them.  
It’s time to populate the gallery with markup.

Use the `images` array of objects and the following `HTML` template for a gallery item.  
In your JavaScript code, generate the markup for the items and then insert all the markup inside `ul.gallery`.  
Do not add any other HTML tags beyond those included in this template.

```html
<li class="gallery-item">
  <a class="gallery-link" href="large-image.jpg">
    <img
      class="gallery-image"
      src="small-image.jpg"
      data-source="large-image.jpg"
      alt="Image description"
    />
  </a>
</li>
```

- The `src` attribute of the `<img>` tag should point to the small version of the image.
- Use the image description for the `alt` attribute.
- The link to the large image should be stored in a `data-source` attribute on the `<img>` element and also set in the `href` of the enclosing `<a>` tag.
- Note that the image is wrapped in a link whose `href` points to the image file. Clicking it could trigger a download in the user's browser. Prevent this default behavior.

#### 4 – Styles

Add gallery styling according to the design layout.

#### 5 – Delegation

Now it's time to add functionality to listen for clicks on gallery items and get the large image URL when clicked.  
Use event delegation on `ul.gallery`. For now, on click, just log the large image URL to the console.

#### 6 – Library Integration

The [basicLightbox](https://github.com/electerious/basicLightbox/tree/master) library provides a fully functional modal window, perfect for this task.  
Use the [jsdelivr CDN](https://www.jsdelivr.com/package/npm/basiclightbox?path=dist) and include the minified (`.min`) JS and CSS files in your HTML.

#### 7 – Modal Window

Update your code so that clicking a gallery item opens a modal window using the library.  
To learn how to initialize and use the modal in your code, check the [documentation](https://github.com/electerious/basicLightbox#readme) and [examples](https://basiclightbox.electerious.com/).

#### 8 – Large Image

Use your code to get the large image URL and replace the `src` of the `<img>` element inside the modal before opening it.  
Use the ready-made modal markup with an image from the [basicLightbox examples](https://basiclightbox.electerious.com/).

#### What the mentor will check:

- The live page displays a gallery of images from the `images` array.
- The gallery is styled according to the design layout.
- Gallery items are created dynamically in JavaScript.
- Event delegation is used to listen for clicks on gallery items.
- Clicking on gallery items without the modal does nothing by default.
- The `basicLightbox` library is included.
- Clicking a gallery item opens the modal window with the enlarged image that was clicked.

---

**Live page: [GitHub Pages](https://akinaru72.github.io/goit-js-hw-08/)**
