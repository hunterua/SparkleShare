SUBDIRS =	Linux

ASSEMBLY = SparkleShare
TARGET = exe

LINK = $(REF_SPARKLESHARE) $(NOTIFY_SHARP_LIBS) $(WEBKIT_SHARP_LIBS)

if HAVE_APP_INDICATOR
BUILD_DEFINES="-define:HAVE_APP_INDICATOR"
endif

SOURCES =  \
	Program.cs \
	SparkleAboutController.cs \
	SparkleBubblesController.cs \
	SparkleControllerBase.cs \
	SparkleEventLogController.cs \
	SparkleExtensions.cs \
	SparkleInvite.cs \
	SparkleOptions.cs \
	SparklePlugin.cs \
	SparkleSetupController.cs \
	SparkleStatusIconController.cs

include $(top_srcdir)/build/build.mk
	
install-data-hook:
	update-desktop-database
	echo "Installed protocol handler sparkleshare://"
