[http://www.github.com/](http://www.github.com/)

## Welcome to hypervvik's Page

You can use the [editor on GitHub](https://github.com/vibhuvikrama/hypervvik.github.io/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```
```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

function fancyAlert(arg) {
      if(arg) {
        $.facebox({div:'#foo'})
      }
    }
    

https://www.github.com/vibhuvikrama/hypervvik.github.io/edit/gh-pages/

http://www.github.com/

<!DOCTYPE html>
<html>
  <head>
    <meta charset=UTF-8 />
    <link rel="stylesheet" type="text/css" href="styles.css" />
  </head>
  <body>
    <script src="three.min.js"></script>
    <script src="GLTFLoader.js"></script>
    <script src="OrbitControls.js"></script>
    <script>
      let scene, camera, renderer;

      function init() {

        scene = new THREE.Scene();
        scene.background = new THREE.Color(0xdddddd);

        camera = new THREE.PerspectiveCamera(40,window.innerWidth/window.innerHeight,1,5000);
        camera.rotation.y = 45/180*Math.PI;
        camera.position.x = 800;
        camera.position.y = 100;
        camera.position.z = 1000;

        controls = new THREE.OrbitControls(camera);
        controls.addEventListener('change', renderer);

        hlight = new THREE.AmbientLight (0x404040,100);
        scene.add(hlight);

        directionalLight = new THREE.DirectionalLight(0xffffff,100);
        directionalLight.position.set(0,1,0);
        directionalLight.castShadow = true;
        scene.add(directionalLight);
        light = new THREE.PointLight(0xc4c4c4,10);
        light.position.set(0,300,500);
        scene.add(light);
        light2 = new THREE.PointLight(0xc4c4c4,10);
        light2.position.set(500,100,0);
        scene.add(light2);
        light3 = new THREE.PointLight(0xc4c4c4,10);
        light3.position.set(0,100,-500);
        scene.add(light3);
        light4 = new THREE.PointLight(0xc4c4c4,10);
        light4.position.set(-500,300,500);
        scene.add(light4);

        renderer = new THREE.WebGLRenderer({antialias:true});
        renderer.setSize(window.innerWidth,window.innerHeight);
        document.body.appendChild(renderer.domElement);

        let loader = new THREE.GLTFLoader();
        loader.load('scene.gltf', function(gltf){
          car = gltf.scene.children[0];
          car.scale.set(0.5,0.5,0.5);
          scene.add(gltf.scene);
          animate();
        });
      }
      function animate() {
        renderer.render(scene,camera);
        requestAnimationFrame(animate);
      }
      init();
    </script>
  </body>
</html>

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/vibhuvikrama/hypervvik.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
