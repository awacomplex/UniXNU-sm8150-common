# UniXNU SM8150 support

Qualcomm SM8150 (Snapdragon 855) shared support for UniXNU. Created for the
Samsung Galaxy Note10+ 5G (`d2xq`), modelled on `unixnu-sm7325-common`.

## Scope

| Path | Contents |
| --- | --- |
| `soc.toml` | SoC profile, component selection, kernel layering |
| `configs/sm8150.config` | Shared kernel configuration |
| `dts/sm8150.dtsi` | Shared hardware: CPUs, GIC, timer, UFS, reserved memory |
| `patches/xnu/series` | Ordered SoC patches |
| `kits/` | Shared platform operations (empty for now) |

## Status

Skeleton. Board values are pending the P0 device recon and the SM8150 DTSI in
`huangkaikaihuang/android_kernel_samsung_d2xq`:

- CPU topology and MPIDR order
- GICv3 bases and redistributor stride
- UFS controller base (`1d84000.ufshc` from device cmdline)
- Reserved memory / DRAM span

Do not treat any value here as verified until it is recorded in `porting.toml`.

## Build

Selected through a device repository:

```toml
[board]
soc = "SM8150"
soc_source = "sm8150"
```

and `feeds.toml` pins this repository as `kind = "soc"`.
