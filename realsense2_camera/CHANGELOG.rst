^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package realsense2_camera
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

2.2.6 (2019-05-22)
------------------
* Merge pull request `#2 <https://github.com/LCAS/realsense/issues/2>`_ from IntelRealSense/development
  pull from upstream
* add note to rs_rgbd.launch, reminding users to initially install ros package rgbd_launch.
* Merge branch 'fix_t265_coordinates' into development
* removed global variable _device, based on @akirayou at https://github.com/IntelRealSense/realsense-ros/issues/774#issuecomment-494236047
* Merge branch 'dense_pointcloud' into development
* Merge branch 'abhijitmajumdar-development' into development
* Merge branch 'development' of https://github.com/abhijitmajumdar/realsense into abhijitmajumdar-development
* fixed bug: imu and synced imu are now sent in original device coordinates frames - i.e. gyro_optical_frame, accel_optical_frame, imu_optical_frame. Fix issue for both t265 and d435i with different coordinate systems.
  fixed bug: sending united imu without images enabled.
  add imu_optical_frame_id to nodelet.launch.xml.
* camera_link for t265 is POSE instead of GYRO.
  fix is needed due to the availability of t265 extrinsics.
* fix inserted bug reading from file
* removed lock_guard.
  set_devices_changed_callback called AFTER getDevice()
  Keep checking for devices until device is found - for cases where T265 was momentarily taken by another node at the time of query.
  Add a 3rd, optional camera, to rs_multiple_devices.launch file.
* fix bug in pointcloud. Used to send points with Z=0.
  add feature: _allow_no_texture_points - if set to true, will send points with depth, both with and without texture.
* Merge pull request `#752 <https://github.com/LCAS/realsense/issues/752>`_ from schmidtp1/sync-get-device
  sync get devices
* sync get devices
* add decimation filter at the front of the filter list, before the start of disparity filter
* change frame_id for imu messages to camera_link's coordinates system, same as imu's sync messages.
* Contributors: Abhijit Majumdar, Marc Hanheide, Phillip Schmidt, Sergey Dorodnicov, doronhi

2.2.5 (2019-05-14)
------------------

2.2.4 (2019-04-09)
------------------
* Merge pull request `#1 <https://github.com/LCAS/realsense/issues/1>`_ from RaymondKirk/update-pkg-meta
  Release Realsense ROS
* Added package requirement 'realsense2-sdk' from lcas farm
* Updated maintainers in package.xml files
* fix bug scaling depth. (`#717 <https://github.com/LCAS/realsense/issues/717>`_)
* Contributors: Marc Hanheide, RaymondKirk, doronhi

* Merge pull request `#1 <https://github.com/LCAS/realsense/issues/1>`_ from RaymondKirk/update-pkg-meta
  Release Realsense ROS
* Added package requirement 'realsense2-sdk' from lcas farm
* Updated maintainers in package.xml files
* fix bug scaling depth. (`#717 <https://github.com/LCAS/realsense/issues/717>`_)
* Contributors: Marc Hanheide, RaymondKirk, doronhi
