# push-push-animal-mahjong

## Styling

The page includes prebuilt, minified Tailwind CSS v3.4.19, so it runs without a build step. If you add Tailwind classes that aren't used anywhere yet, regenerate the CSS.

1. In an empty folder outside the repo, create `input.css`:

   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```

2. In the same folder, create `tailwind.config.js` (point `content` at your copy of the game file):

   ```js
   module.exports = {
     content: ['path/to/push_push_animal_mahjong.html'],
   };
   ```

3. Build:

   ```sh
   npm install tailwindcss@3.4.19
   npx tailwindcss -i input.css -c tailwind.config.js -o tailwind.min.css --minify
   ```

4. Replace the contents of `<style id="tailwind-prebuilt">` near the top of `push_push_animal_mahjong.html` with the contents of `tailwind.min.css`.
