^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package ddynamic_reconfigure
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

2.2.4 (2019-04-09)
------------------
* Merge pull request `#1 <https://github.com/LCAS/realsense/issues/1>`_ from RaymondKirk/update-pkg-meta
  Release Realsense ROS
* Added package requirement 'realsense2-sdk' from lcas farm
* Updated maintainers in package.xml files
* Contributors: Marc Hanheide, RaymondKirk

* Merge pull request `#1 <https://github.com/LCAS/realsense/issues/1>`_ from RaymondKirk/update-pkg-meta
  Release Realsense ROS
* Added package requirement 'realsense2-sdk' from lcas farm
* Updated maintainers in package.xml files
* Contributors: Marc Hanheide, RaymondKirk

2.2.3 (2019-04-02)
------------------

2.2.2 (2019-04-01)
------------------
* Export dynamic_reconfigure to dependent packages (`#673 <https://github.com/LCAS/realsense/issues/673>`_)
  @efernandez , thanks for noticing.
  @stwirth thanks for the explanation.
* Contributors: Enrique Fernández Perdomo

2.2.1 (2019-03-07)
------------------
* Fix dependencies of ddynamic_reconfigure (`#624 <https://github.com/LCAS/realsense/issues/624>`_)
* Fix `#628 <https://github.com/LCAS/realsense/issues/628>`_ - added guards around clang-specific pragmas (`#630 <https://github.com/LCAS/realsense/issues/630>`_)
  Also added a guard around an OpenMP pragma
* Contributors: Jarvis Schultz, Stephan

2.2.0 (2019-02-17)
------------------

2.1.4 (2019-01-24)
------------------

2.1.3 (2019-01-01)
------------------
* fix: wrong reference for the gmock dependency (`#546 <https://github.com/LCAS/realsense/issues/546>`_)
  fix: typo on ddynamic_reconfigure
* use ddynamic_reconfigure and support D435i (`#535 <https://github.com/LCAS/realsense/issues/535>`_)
  Add dynamic dynamic reconfigure. That means there are no longer differences in the code between D415, D430, SR300.
  Add dynamic options for filters
  Add support for camera D435i.
  Add clipping_disance option. enabled with parameter: clip_distance. units: meters. Default: no clipping.
  Add linear accel covariance - Default: 0.01
  Add option: unite_imu - send linear acceleration and radial velocity in the same Imu message. Default: True
  Add parameter: hold_back_imu_for_frames. If set to true, hold imu messages that arrived while manipulating frames, until frames are actually sent.
  Comply with librealsense v2.17.0
  Add opensource_tracking.launch - demo that runs realsense2_camera, imu_filter_madgwick, rtabmap and robot_localization to demonstrate Slam with realsense D435i
  Set accel_fps to 250 as this is the new maximal rate in librealsense v2.17.0
  * Add NOTICE file, to emphasize the contribution of the ddynamic_reconfigure project.
  Known Issue: Option for toggling sensor on and off while running is missing.
* Contributors: Thiago de Freitas, doronhi

2.1.2 (2018-12-06)
------------------

2.1.1 (2018-11-01)
------------------

2.1.0 (2018-09-27)
------------------

2.0.4 (2018-08-29)
------------------

2.0.3 (2018-03-29)
------------------

2.0.2 (2018-01-31)
------------------

2.0.1 (2017-11-02)
------------------

2.0.0 (2017-09-17)
------------------
