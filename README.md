## STM32 External Crystal Library of SystemClock_Config

This library provides the necessary files for using an external 8MHz crystal with generic STM32 controllers in the stm32Duino environment. By using an external crystal, more accurate timing can be achieved compared to the internal oscillator used by most stm32Duino controllers.

## Usage

To use the 8MHz crystal with a controller such as the STM32F446, include the following line in your code:

```#include "meClock_F446.h"```

This library includes the `SystemClock_Config` files for the following STM32 families:

- STM32F446
- STM32F413
- STM32L4 series
- STM32G4 series

Note that for the STM32G4 series, the default stm32Duino crystal setting is 24MHz, whereas the other families use 8MHz. The `SystemClock_Config` provided in this library is configured for 8MHz. If using the STM32G4 series with this library, an additional file named `build_opt` is required in the project directory with the following setting for an 8MHz crystal:

```-DHSE_VALUE=8000000```

## License

This library is licensed under the MIT License. See the `LICENSE` file for more information.

