# HTML & CSS Animation Project

This is a personal project exploring visual effects with CSS and HTML. The main goal is to create an interactive animation when hovering over an image, changing its perspective and revealing another image with a smooth transition—all without using JavaScript.

## Technologies Used

- **HTML**: For the page structure.  
- **CSS**: For styling and animations.

## How It Works

1. Inside an `<article>`, two images are included:
   - The first image serves as a background and has a shadow to add depth.  
   - The second image (Tux) is hidden by default and overlays the first when hovered.

2. The Tux image is positioned with `position: absolute` to overlay the first image.

3. `opacity: 0` keeps Tux invisible until the user hovers over the article.

4. On hover:
   - A 3D transformation (`perspective`, `rotateX`, `translateY`, `translateZ`) is applied to the background image.  
   - Tux’s opacity changes to `1` and it moves slightly upward.  
   - A gradient darkens the lower part of the article, creating a more immersive effect.

## Files

### `index.html`

Basic structure of the document:

```html
<article>
    <img src="./Imgs/debian_wallpaper.jpg" alt="Debian Background">
    <img src="./Imgs/tux.png" alt="Tux">
</article>
style.css
Styles and animations:

article:hover {
    transform:
        perspective(250px)
        rotateX(10deg)
        translateY(-5%)
        translateZ(0);
}

article:hover img:last-child {
    opacity: 1;
    transform: translateY(10%);
}
How to Use
Clone this repository:

git clone https://github.com/mi-usuario/mi-repositorio.git
Open index.html in your favorite browser.
