#
# Makefile for Bosch sensor driver.
#
obj-y += bstclass.o

obj-$(CONFIG_SENSORS_BMA2X2)	+= bma2x2.o

ifeq ($(CONFIG_SENSORS_BMA2X2_ENABLE_INT1),y)
	EXTRA_CFLAGS += -DBMA2X2_ENABLE_INT1
endif

ifeq ($(CONFIG_BOSCH_BMA2X2_ENABLE_INT2),y)
	EXTRA_CFLAGS += -DBMA2X2_ENABLE_INT2
endif


obj-$(CONFIG_SENSORS_BMG)    += bmg160_driver.o bmg160.o
ifeq ($(CONFIG_SENSORS_BMG_FIFO),y)
	EXTRA_CFLAGS += -DBMG_USE_FIFO -DBMG_USE_BASIC_I2C_FUNC
endif


obj-$(CONFIG_SENSORS_BMM050)    += bmm050_driver.o bmm050.o
EXTRA_CFLAGS += -DBMM_USE_BASIC_I2C_FUNC -DCONFIG_BMM_USE_PLATFORM_DATA


obj-$(CONFIG_SENSORS_BMP18X)      += bmp18x-core.o bmp18x-i2c.o

obj-$(CONFIG_SENSORS_BMP280)      += bmp280_core.o bmp280.o
obj-$(CONFIG_SENSORS_BMP280_I2C)  += bmp280_i2c.o
obj-$(CONFIG_SENSORS_BMP280_SPI)  += bmp280_spi.o
ifeq ($(CONFIG_SENSORS_BMP280_I2C),y)
	EXTRA_CFLAGS += -DBMP_USE_BASIC_I2C_FUNC
endif

