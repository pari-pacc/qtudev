find_package(Libudev REQUIRED)

liri_add_module(Qt5Udev
    DESCRIPTION
        "Qt style API for udev"
    MODULE_NAME
        Qt5Udev
    VERSIONED_MODULE_NAME
        Qt5Udev
    SOURCES
        logindseat.cpp
        logindseat_p.h
        udev.cpp
        udevdevice.cpp
        udevdevice.h
        udevdevice_p.h
        udevenumerate.cpp
        udevenumerate.h
        udevenumerate_p.h
        udev.h
        udevmonitor.cpp
        udevmonitor.h
        udevmonitor_p.h
        udev_p.h
    DEFINES
        QT_NO_CAST_FROM_ASCII
        QT_NO_FOREACH
    PUBLIC_LIBRARIES
        Qt5::Core
    LIBRARIES
        Qt5::DBus
        PkgConfig::Libudev
    PKGCONFIG_DEPENDENCIES
        Qt5Core
        libudev
)

liri_finalize_module(Qt5Udev)
