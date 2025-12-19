# JSON Font Collection for ThreeJS FontLoader


### You can convert ttf to json(threejs font)
> https://gero3.github.io/facetype.js/


### Use tips
You need to change the URL from github.com to raw.githubusercontent.com

``` javascript
const fontLoader = new THREEADDON.FontLoader();
fontLoader.load('https://raw.githubusercontent.com/Dave-Redbrick/Font/main/EN/Roboto_Regular.json', (font) => {
    const geometry = new THREEADDON.TextGeometry(
        'I Love ThreeJS',
       {
           font: font,
           size: 1,
           height: 0,
        //   curveSegments: 12,
       }
    );
    geometry.computeBoundingBox();
    const xMid = -0.5 * (geometry.boundingBox.max.x - geometry.boundingBox.min.x);
    geometry.translate(xMid, 0, 0);

    const material = new THREE.MeshBasicMaterial({
        color: 0xffffff, 
        wireframe: false,
    });

    const mesh = new THREE.Mesh(geometry, material);
    mesh.position.set(0, 2, 0);
    WORLD.add(mesh); // scene.add(mesh);
});
```

### Font List

##### KR/EN
- BM_HANNA_11yrs_Regular
- Maplestory_Light
- SB_Aggro_Medium_Regular

##### EN
- Roboto_Regular
- Inter_Regular
- Junegull_Regular
- Tilt Neon_Regular
