# Copyright 2019-2020, Collabora, Ltd.
# SPDX-License-Identifier: BSL-1.0

driver_libs = []
driver_deps = []

if libusb.found()
	driver_deps += [libusb]
endif

if libjpeg.found()
	driver_deps += [libjpeg]
endif

if 'dummy' in drivers
	driver_libs += [lib_drv_dummy]
endif

if 'hdk' in drivers
	driver_libs += [lib_drv_hdk]
endif

if 'hydra' in drivers
	driver_libs += [lib_drv_hydra]
endif

if 'ns' in drivers
	driver_libs += [lib_drv_ns]
endif

if 'ohmd' in drivers
	driver_libs += [lib_drv_ohmd]
endif

if 'psmv' in drivers
	driver_libs += [lib_drv_psmv]
endif

if 'psvr' in drivers
	driver_libs += [lib_drv_psvr]
endif

if 'v4l2' in drivers
	driver_libs += [lib_drv_v4l2]
	driver_deps += [v4l2]
endif

if 'vive' in drivers
	driver_libs += [lib_drv_vive]
endif

subdir('common')
subdir('openxr')
subdir('cli')

if sdl2.found()
	subdir('gui')
endif
