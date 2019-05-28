CHANGELOG
=========

Raster Vision 0.10
-----------------

Raster Vision 0.10.0
~~~~~~~~~~~~~~~~~~~

Features
^^^^^^^^^^^^

- Add confusion matrix as metric for semantic segmentation `#788 <https://github.com/azavea/raster-vision/pull/788>`__
- Handle "ignore" class for semantic segmentation `#783 <https://github.com/azavea/raster-vision/pull/783>`__

Bug Fixes
^^^^^^^^^

- Fixed issue with configuration not being able to read lists `#784 <https://github.com/azavea/raster-vision/pull/784>`__

Raster Vision 0.9
-----------------

Raster Vision 0.9.0
~~~~~~~~~~~~~~~~~~~

Features
^^^^^^^^
- Add requester_pays RV config option `#762 <https://github.com/azavea/raster-vision/pull/762>`_
- Unify Docker scripts `#743 <https://github.com/azavea/raster-vision/pull/743>`_
- Switch default branch to master `#726 <https://github.com/azavea/raster-vision/pull/726>`_
- Merge GeoTiffSource and ImageSource into RasterioSource `#723 <https://github.com/azavea/raster-vision/pull/723>`_
- Simplify/clarify/test/validate RasterSource `#721 <https://github.com/azavea/raster-vision/pull/721>`_
- Simplify and generalize geom processing `#711 <https://github.com/azavea/raster-vision/pull/711>`_
- Predict zero for nodata pixels on semantic segmentation `#701 <https://github.com/azavea/raster-vision/pull/701>`_
- Add support for evaluating vector output with AOIs `#698 <https://github.com/azavea/raster-vision/pull/698>`_
- Conserve disk space when dealing with raster files `#692 <https://github.com/azavea/raster-vision/pull/692>`_
- Optimize StatsAnalyzer `#690 <https://github.com/azavea/raster-vision/pull/690>`_
- Include per-scene eval metrics `#641 <https://github.com/azavea/raster-vision/pull/641>`_
- Make and save predictions and do eval chip-by-chip `#635 <https://github.com/azavea/raster-vision/pull/635>`_
- Decrease semseg memory usage `#630 <https://github.com/azavea/raster-vision/pull/630>`_
- Add support for vector tiles in .mbtiles files `#601 <https://github.com/azavea/raster-vision/pull/601>`_
- Add support for getting labels from zxy vector tiles `#532 <https://github.com/azavea/raster-vision/pull/532>`_
- Remove custom ``__deepcopy__`` implementation from ``ConfigBuilder``\s. `#567 <https://github.com/azavea/raster-vision/pull/567>`_
- Add ability to shift raster images by given numbers of meters. `#573 <https://github.com/azavea/raster-vision/pull/573>`_
- Add ability to generate GeoJSON segmentation predictions. `#575 <https://github.com/azavea/raster-vision/pull/575>`_
- Add ability to run the DeepLab eval script.  `#653 <https://github.com/azavea/raster-vision/pull/653>`_
- Submit CPU-only stages to a CPU queue on Aws.  `#668 <https://github.com/azavea/raster-vision/pull/668>`_
- Parallelize CHIP and PREDICT commands  `#671 <https://github.com/azavea/raster-vision/pull/671>`_
- Refactor ``update_for_command`` to split out the IO reporting into ``report_io``. `#671 <https://github.com/azavea/raster-vision/pull/671>`_
- Add Multi-GPU Support to DeepLab Backend `#590 <https://github.com/azavea/raster-vision/pull/590>`_
- Handle multiple AOI URIs `#617 <https://github.com/azavea/raster-vision/pull/617>`_
- Give ``train_restart_dir`` Default Value `#626 <https://github.com/azavea/raster-vision/pull/626>`_
- Use ```make`` to manage local execution `#664 <https://github.com/azavea/raster-vision/pull/664>`_
- Optimize vector tile processing  `#676 <https://github.com/azavea/raster-vision/pull/676>`_

Bug Fixes
^^^^^^^^^
- Fix Deeplab resume bug: update path in checkpoint file `#756 <https://github.com/azavea/raster-vision/pull/756>`_
- Allow Spaces in ``--channel-order`` Argument `#731 <https://github.com/azavea/raster-vision/pull/731>`_
- Fix error when using predict packages with AOIs `#674 <https://github.com/azavea/raster-vision/pull/674>`_
- Correct checkpoint name `#624 <https://github.com/azavea/raster-vision/pull/624>`_
- Allow using default stride for semseg sliding window  `#745 <https://github.com/azavea/raster-vision/pull/745>`_
- Fix filter_by_aoi for ObjectDetectionLabels `#746 <https://github.com/azavea/raster-vision/pull/746>`_
- Load null channel_order correctly `#733 <https://github.com/azavea/raster-vision/pull/733>`_
- Handle Rasterio crs that doesn't contain EPSG `#725 <https://github.com/azavea/raster-vision/pull/725>`_
- Fixed issue with saving semseg predictions for non-georeferenced imagery `#708 <https://github.com/azavea/raster-vision/pull/708>`_
- Fixed issue with handling width > height in semseg eval `#627 <https://github.com/azavea/raster-vision/pull/627>`_
- Fixed issue with experiment configs not setting key names correctly `#576 <https://github.com/azavea/raster-vision/pull/576>`_
- Fixed issue with Raster Sources that have channel order `#576 <https://github.com/azavea/raster-vision/pull/576>`_


Raster Vision 0.8
-----------------

Raster Vision 0.8.1
~~~~~~~~~~~~~~~~~~~

Bug Fixes
^^^^^^^^^
- Allow multiploygon for chip classification `#523 <https://github.com/azavea/raster-vision/pull/523>`_
- Remove unused args for AWS Batch runner `#503 <https://github.com/azavea/raster-vision/pull/503>`_
- Skip over lines when doing chip classification, Use background_class_id for scenes with no polygons `#507 <https://github.com/azavea/raster-vision/pull/507>`_
- Fix issue where ``get_matching_s3_keys`` fails when ``suffix`` is ``None`` `#497 <https://github.com/azavea/raster-vision/pull/497>`_
