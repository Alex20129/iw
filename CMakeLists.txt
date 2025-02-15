CMAKE_MINIMUM_REQUIRED(VERSION 3.5)

PROJECT(iw)

SET(CMAKE_INCLUDE_CURRENT_DIR ON)

SET(CMAKE_AUTOUIC ON)
SET(CMAKE_AUTOMOC ON)

SET(CMAKE_CXX_FLAGS "-O0 -no-pie -Wall")

LINK_LIBRARIES(pthread nl-3 nl-genl-3)

INCLUDE_DIRECTORIES("/usr/include/libnl3")

ADD_DEFINITIONS("-DCONFIG_LIBNL30")

ADD_EXECUTABLE(${CMAKE_PROJECT_NAME}
	ieee80211.h
	iw.h
	nl80211.h
	sha256.h
	ap.c
	bitrate.c
	bloom.c
	coalesce.c
	connect.c
	cqm.c
	event.c
	ftm.c
	genl.c
	hwsim.c
	ibss.c
	info.c
	interface.c
	iw.c
	link.c
	measurements.c
	mesh.c
	mgmt.c
	mpath.c
	mpp.c
	nan.c
	ocb.c
	offch.c
	p2p.c
	phy.c
	ps.c
	reason.c
	reg.c
	roc.c
	sar.c
	scan.c
	sections.c
	sha256.c
	station.c
	status.c
	survey.c
	util.c
	vendor.c
	wowlan.c)
