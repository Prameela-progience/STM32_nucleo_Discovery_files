################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (13.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F2xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := Sensor_f207_as_a transmiter_CAN1_cmm
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
Sensor_f207_as_a\ transmiter_CAN1_cmm.elf \

MAP_FILES += \
Sensor_f207_as_a\ transmiter_CAN1_cmm.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Sensor_f207_as_a\ transmiter_CAN1_cmm.list \


# All Target
all: main-build

# Main-build Target
main-build: Sensor_f207_as_a\ transmiter_CAN1_cmm.elf secondary-outputs

# Tool invocations
Sensor_f207_as_a\ transmiter_CAN1_cmm.elf Sensor_f207_as_a\ transmiter_CAN1_cmm.map: $(OBJS) $(USER_OBJS) /home/sravanthi/STM32CubeIDE\ (2)/new_workspace/Sensor_f207_as_a\ transmiter_CAN1_cmm/STM32F207ZGTX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "Sensor_f207_as_a transmiter_CAN1_cmm.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/sravanthi/STM32CubeIDE (2)/new_workspace/Sensor_f207_as_a transmiter_CAN1_cmm/STM32F207ZGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Sensor_f207_as_a transmiter_CAN1_cmm.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -u _printf_float -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Sensor_f207_as_a\ transmiter_CAN1_cmm.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Sensor_f207_as_a transmiter_CAN1_cmm.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) Sensor_f207_as_a\ transmiter_CAN1_cmm.elf Sensor_f207_as_a\ transmiter_CAN1_cmm.list Sensor_f207_as_a\ transmiter_CAN1_cmm.map Sensor_f207_as_a\\ transmiter_CAN1_cmm.elf default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
