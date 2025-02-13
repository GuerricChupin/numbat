<!-- This file is autogenerated! Do not modify it -->

# XKCD 2812
<a href="https://numbat.dev/?q=%23+Solar+panel+placement%0A%23%0A%23+Solar+energy+tip%3A+To+maximize+sun+exposure%2C+always%0A%23+orient+your+panels+downward+and+install+them+on+the%0A%23+surface+of+the+sun.%0A%23%0A%23+https%3A%2F%2Fxkcd.com%2F2812%2F%0A%23%0A%23+%5B1%5D+https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FSolar_luminosity%0A%23+%5B2%5D+https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FSun%0A%0Alet+net_metering_rate+%3D+%24+0.20+%2F+kWh%0Alet+panel_area+%3D+1+m%C2%B2%0Alet+panel_efficiency+%3D+20+%25%0A%0Afn+savings%28i%3A+Irradiance%29+-%3E+Money+%2F+Time+%3D%0A++++net_metering_rate+%C3%97+i+%C3%97+panel_area+%C3%97+panel_efficiency+-%3E+%24%2Fyear%0A%0Aprint%28%22Option+A%3A+On+the+roof%2C+south+facing%22%29%0A%0Alet+savings_a+%3D+savings%284+kWh%2Fm%C2%B2%2Fday%29%0A%0Aprint%28savings_a+%7C%3E+round%29%0A%0Aprint%28%29%0Aprint%28%22Option+B%3A+On+the+sun%2C+downward+facing%22%29%0A%0Adimension+Luminosity+%3D+Power%0A%0Alet+sun_luminosity%3A+Luminosity+%3D+3.828e26+W++%23+%5B1%5D%0Alet+sun_area%3A+Area+%3D+6.09e12+km%5E2++++++++++++%23+%5B2%5D%0A%0Alet+savings_b+%3D+savings%28sun_luminosity+%2F+sun_area%29%0A%0Aprint%28savings_b+%7C%3E+round%29%0A"><i class="fa fa-play"></i> Run this example</a>

``` numbat
# Solar panel placement
#
# Solar energy tip: To maximize sun exposure, always
# orient your panels downward and install them on the
# surface of the sun.
#
# https://xkcd.com/2812/
#
# [1] https://en.wikipedia.org/wiki/Solar_luminosity
# [2] https://en.wikipedia.org/wiki/Sun

let net_metering_rate = $ 0.20 / kWh
let panel_area = 1 m²
let panel_efficiency = 20 %

fn savings(i: Irradiance) -> Money / Time =
    net_metering_rate × i × panel_area × panel_efficiency -> $/year

print("Option A: On the roof, south facing")

let savings_a = savings(4 kWh/m²/day)

print(savings_a |> round)

print()
print("Option B: On the sun, downward facing")

dimension Luminosity = Power

let sun_luminosity: Luminosity = 3.828e26 W  # [1]
let sun_area: Area = 6.09e12 km^2            # [2]

let savings_b = savings(sun_luminosity / sun_area)

print(savings_b |> round)
```

<p align="center" style="margin-top: 2em"><a href="https://xkcd.com/2812/"><img src="https://imgs.xkcd.com/comics/solar_panel_placement.png" alt="XKCD 2812" style="max-width: 100%"></a><br>Source: <a href="https://xkcd.com/2812/">https://xkcd.com/2812/</a></p>
