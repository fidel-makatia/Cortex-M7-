################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F7xx_HAL_Driver/Src/subdir.mk
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
UART_with_Timers.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
UART_with_Timers.list \

OBJCOPY_BIN += \
UART_with_Timers.bin \


# All Target
all: UART_with_Timers.elf secondary-outputs

# Tool invocations
UART_with_Timers.elf: $(OBJS) $(USER_OBJS) C:\Users\t_makaf\STM32CubeIDE\workspace_1.3.0\UART_with_Timers\STM32F746ZGTX_FLASH.ld
	arm-none-eabi-gcc -o "UART_with_Timers.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m7 -T"C:\Users\t_makaf\STM32CubeIDE\workspace_1.3.0\UART_with_Timers\STM32F746ZGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="UART_with_Timers.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv5-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

UART_with_Timers.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "UART_with_Timers.list"
	@echo 'Finished building: $@'
	@echo ' '

UART_with_Timers.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "UART_with_Timers.bin"
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
