################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Lib/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: Example_VirtualSerialDevice.axf

# Tool invocations
Example_VirtualSerialDevice.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"/Users/CS_Toku/Documents/LPCXpresso_7.3.0/sagyou/workspace/CDL" -L"/Users/CS_Toku/Documents/LPCXpresso_7.3.0/sagyou/workspace/BSP" -L"/Users/CS_Toku/Documents/LPCXpresso_7.3.0/sagyou/workspace/LPCUSBlib" -L"/Users/CS_Toku/Documents/LPCXpresso_7.3.0/sagyou/workspace/LCDlib/Debug" -Xlinker -Map="Example_VirtualSerialDevice.map" -Xlinker --gc-sections -mcpu=cortex-m0 -mthumb -T "Example_VirtualSerialDevice_LPC11Uxx.ld" -o "Example_VirtualSerialDevice.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(OBJS)$(C_DEPS)$(EXECUTABLES) Example_VirtualSerialDevice.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "Example_VirtualSerialDevice.axf" ; arm-none-eabi-objcopy -O binary "Example_VirtualSerialDevice.axf" "Example_VirtualSerialDevice.bin" ; checksum -p LPC11U24_401 -d "Example_VirtualSerialDevice.bin"
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY: post-build

-include ../makefile.targets
