################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32L4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
meh-to-master-led.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
meh-to-master-led.list \

OBJCOPY_BIN += \
meh-to-master-led.bin \


# All Target
all: meh-to-master-led.elf secondary-outputs

# Tool invocations
meh-to-master-led.elf: $(OBJS) $(USER_OBJS) C:\Users\ruthg\STM32CubeIDE\workspace_1.2.0\meh-to-master-led\STM32L476VGTX_FLASH.ld
	arm-none-eabi-gcc -o "meh-to-master-led.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\ruthg\STM32CubeIDE\workspace_1.2.0\meh-to-master-led\STM32L476VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="meh-to-master-led.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

meh-to-master-led.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "meh-to-master-led.list"
	@echo 'Finished building: $@'
	@echo ' '

meh-to-master-led.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "meh-to-master-led.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
