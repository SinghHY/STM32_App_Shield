# STM32_App_Shield
mbed Application Shield with STM32

First Test

int main(void)
{

  HAL_Init();
  SystemClock_Config();
  MX_GPIO_Init();

  HAL_GPIO_WritePin(GREEN_Led_GPIO_Port, GREEN_Led_Pin, GPIO_PIN_SET);
  HAL_GPIO_WritePin(RED_Led_GPIO_Port, RED_Led_Pin, GPIO_PIN_SET);

  while (1)
  {
	  HAL_GPIO_TogglePin(GPIOA, BLUE_Led_Pin);
	  HAL_Delay(500);
  }

}