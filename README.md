# GSVPanoPointCloud.js

A JavaScript library that downloads and extracts 3d point cloud from Google Street View. This is an extension of GSVPanoDepth.js, which can be found in the following repo:  https://github.com/proog128/GSVPanoDepth.js .

## Usage

```html
<script src="https://maps.googleapis.com/maps/api/js?v=3.exp&sensor=false" type="text/javascript"></script>
<script src="jquery.min.js" type="text/javascript"></script>
<script src="jquery.base64.min.js" type="text/javascript"></script>
<script src="zpipe.min.js" type="text/javascript"></script>
<script src="GSVPanoPointCloud.js" type="text/javascript"></script>
```

```js
var pointCloudLoader = new GSVPANO.PanoPointCloudLoader();

pointCloudLoader.onPointCloudLoad = function() {

    // Returns depth map in the following format:
    //
    // this.pointCloud.width: width of depth map in pixels
    // this.pointCloud.height: height of depth map in pixels
    // this.pointCloud.pointCloud: Float32Array of size width*height that contains the depth at each pixel

};

panoLoader.load(new google.maps.LatLng(42.345601, -71.098348));
```

## Requirements

* jQuery
* [jquery-base64](https://github.com/carlo/jquery-base64)
* [zpipe](https://github.com/richardassar/zpipe)
* [GSVPano.js](https://github.com/spite/GSVPano.js) (slightly modified to include panorama ID in results)

## License

MIT License
