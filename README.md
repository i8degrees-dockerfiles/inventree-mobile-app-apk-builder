InvenTree mobile app: APK builder (Android)
==================================

**NOTE(JEFF):** This repository is a fork of the [upstream repository][20].

This repository provides a Dockerfile to automate the build process for the [InvenTree Android app][0], resulting in an APK file placed in the `dist` directory.

In the releases section, one can download pre-built APK files, maintained on a best effort basis.

Requirements
------------

*   Docker installed
    

Usage
-----

1.  `mkdir -p ./dist`
    
2.  `docker build -t inventree-dockerbuild .`
    
3.  `docker run -v $(pwd)/dist:/output -ti --rm inventree-dockerbuild`
    

Output
------

*   The generated APK file will be available in the `dist` subdirectory.
    

Notes
-----

*   The Dockerfile clones the [InvenTree Android app][10] source and compiles it.   
    
*   The `dist` directory is mapped to extract the generated APK from the container.
    

Troubleshooting
---------------

*   Ensure adequate disk space and correct dependency versions.
    
*   Run docker logs for build errors.
    

License
-------

Licensed under the MIT License. See the LICENSE file for more information.

Foot Notes
----------

[0]: https://play.google.com/store/apps/details?id=inventree.inventree_app
[10]: https://github.com/inventree/inventree-app
[20]: https://github.com/laurensramandt/inventree-mobile-app-apk-builder
