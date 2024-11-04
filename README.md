# [`orange-i` module](https://github.com/viam-modules/orange-i)

This [orange-i module](https://app.viam.com/module/viam/orange-i) implements a orange-i [orangepi board](<LINK TO HARDWARE>), used for <DESCRIPTION> using the [`rdk:component:board` API](https://docs.viam.com/appendix/apis/components/board/).

> [!NOTE]
> Before configuring your board, you must [create a machine](https://docs.viam.com/cloud/machines/#add-a-new-machine).

## Configure your orangepi board

Navigate to the [**CONFIGURE** tab](https://docs.viam.com/configure/) of your [machine](https://docs.viam.com/fleet/machines/) in the [Viam app](https://app.viam.com/).
[Add board / orange-i:orangepi to your machine](https://docs.viam.com/configure/#components).

On the new component panel, copy and paste the following attribute template into your board's attributes field:

```json
{
  <ATTRIBUTES>
}
```
> [!NOTE]
> For more information, see [Configure a Machine](https://docs.viam.com/configure/).

### Attributes

The following attributes are available for `viam:orange-i:orangepi` boards:

<EXAMPLE !!>
| Attribute | Type | Required? | Description |
| --------- | ---- | --------- | ----------  |
| `i2c_bus` | string | **Required** | The index of the I<sup>2</sup>C bus on the board that the board is wired to. |
| `i2c_address` | string | Optional | Default: `0x77`. The [I<sup>2</sup>C device address](https://learn.adafruit.com/i2c-addresses/overview) of the board. |

## Example configuration

### `viam:orange-i:orangepi`
```json
  {
     "name": "<your-orange-i-orangepi-board-name>",
      "model": "viam:orange-i:orangepi",
      "type": "board",
      "namespace": "rdk",
      "attributes": {
      },
      "depends_on": []
  }
```

### Next Steps
- To test your board, expand the **TEST** section of its configuration pane or go to the [**CONTROL** tab](https://docs.viam.com/fleet/control/).
- To write code against your board, use one of the [available SDKs](https://docs.viam.com/sdks/).
- To view examples using a board component, explore [these tutorials](https://docs.viam.com/tutorials/).