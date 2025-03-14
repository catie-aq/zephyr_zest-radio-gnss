# Zest_Radio_GNSS

Zest_Radio_GNSS board for Zephyr OS.

## Usage

This board enables the following component:

- [Quectel L86](https://www.quectel.com/product/gnss-l86/) GNSS module.

💡 This driver should also be added to your workspace:

- [Quectel L86 driver](https://github.com/catie-aq/zephyr_quectel-l86).

:pushpin: This shield defines:

- a GNSS module device: `l86_zest_radio_gnss_<port>`.

:triangular_ruler: To use this shield:

- Update your device tree by adding the `ZEST_RADIO_GNSS(port)` macro to the `app.overlay` file.\
  Replace `port` with the number of the Zest_Core port to which the shield is connected, e.g.:

  ```c
  ZEST_RADIO_GNSS(1) /* Zest_Radio_GNSS connected to Zest_Core first port */
  ```

- Activate support for the shield by adding `--shield zest_radio_gnss` to the west command.
