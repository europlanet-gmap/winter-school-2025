# QGIS Custom Projections

## IAU 2015 & QGIS

**NOTE:** IAU\_2015 projections are now embedded in **PROJ** and **QGIS**. Earlier versions of **QGIS for MacOS** (3.32) had issues with IAU\_2015 CRS lookup, but this has been resolved in **QGIS 3.34** for all platforms (Windows, Linux, MacOS). See the related discussion [here](https://github.com/qgis/QGIS/issues/54514).

---

### QGIS Project Settings

It may be useful to set **QGIS project properties** accordingly when working with planetary mapping data.

### Adding Custom Projections

To add **custom projections** manually in QGIS:

1. Go to **Settings → Custom Projections**
2. Add the relevant **Proj4** or **WKT2** string
3. Validate the projection using the **Validate** button
4. Save it to the user profile by clicking **OK**

For a **user-level custom CRS**, refer to the individual mapping areas and **Solar System bodies** at: [Europlanet GMAP Winter School 2025](https://github.com/europlanet-gmap/winter-school-2025).

---

## Coordinate Reference Systems (CRS) for Mapping Projects

For convenience, the CRS for each planetary mapping project are listed below.

### **Introductory Mappy/OPC Mapping Project**

[Project link](https://github.com/europlanet-gmap/winter-school-2024/blob/main/mappy-opencratertool/mappy-opencratertool_data_info_2024-GMAP-winter-school.md)

#### Proj4 CRS

```
+proj=eqc +lat_ts=0 +lat_0=0 +lon_0=0 +x_0=0 +y_0=0 +R=1737400 +units=m +no_defs +type=crs
```

#### WKT CRS

```
PROJCRS["unknown",
    BASEGEOGCRS["unknown",
        DATUM["unknown",
            ELLIPSOID["unknown",1737400,0,
                LENGTHUNIT["metre",1,
                    ID["EPSG",9001]]]],
        PRIMEM["Reference meridian",0,
            ANGLEUNIT["degree",0.0174532925199433,
                ID["EPSG",9122]]]],
    CONVERSION["unknown",
        METHOD["Equidistant Cylindrical (Spherical)",
            ID["EPSG",1029]],
        PARAMETER["Latitude of 1st standard parallel",0,
            ANGLEUNIT["degree",0.0174532925199433],
            ID["EPSG",8823]],
        PARAMETER["Longitude of natural origin",0,
            ANGLEUNIT["degree",0.0174532925199433],
            ID["EPSG",8802]],
        PARAMETER["False easting",0,
            LENGTHUNIT["metre",1],
            ID["EPSG",8806]],
        PARAMETER["False northing",0,
            LENGTHUNIT["metre",1],
            ID["EPSG",8807]]],
    CS[Cartesian,2],
        AXIS["(E)",east,
            ORDER[1],
            LENGTHUNIT["metre",1,
                ID["EPSG",9001]]],
        AXIS["(N)",north,
            ORDER[2],
            LENGTHUNIT["metre",1,
                ID["EPSG",9001]]]]
```

---

### **Venus Mapping Project**

[Project link](https://github.com/europlanet-gmap/winter-school-2025/tree/main/venus)

#### Proj4 CRS

```
+proj=merc +lat_ts=-40 +lon_0=-90 +x_0=0 +y_0=0 +R=6051000 +units=m +no_defs +type=crs
```

#### WKT CRS

*(See README for full details)*

---

### **Mercury Mapping Project**

[Project link](https://github.com/europlanet-gmap/winter-school-2025/tree/main/mercury)

#### Proj4 CRS

```
+proj=longlat +R=2439700 +no_defs +type=crs
```

#### WKT CRS

*(See README for full details)*

---

### **Moon Mapping Project**

[Project link](https://github.com/europlanet-gmap/winter-school-2025/tree/main/moon)

#### Proj4 CRS

```
+proj=longlat +R=1737400 +no_defs +type=crs
```

#### WKT CRS

*(See README for full details)*

---

### **Mars Mapping Project**

[Project link](https://github.com/europlanet-gmap/winter-school-2025/tree/main/mars)

#### Proj4 CRS

```
+proj=longlat +a=3396190 +rf=169.894447223612 +no_defs +type=crs
```

#### WKT CRS

*(See README for full details)*

---

## Example from 2023 Mars Mapping Project

For reference, see the [2023 Mars Mapping Project](https://github.com/europlanet-gmap/winter-school-2023/blob/main/mars/mars_data_info_2023-GMAP-winter-school.md#crs).

One can name the projection **Mars-Equirectangular** (or any other suitable name), then:

1. Add the **Proj4** code
2. Validate it using the "Validate" button
3. Save it to the user profile

**Proj4 Code:**

```
+proj=eqc +lat_ts=0 +lat_0=0 +lon_0=0 +x_0=0 +y_0=0 +R=3396190 +units=m +no_defs +type=crs
```

---

## Recommended CRS Format

For ease of use, **Proj4 codes** are provided, but **WKT2** is preferable as it embeds more metadata than Proj4.

For more details, see:

- [PROJ FAQ](https://proj.org/faq.html#what-is-the-best-format-for-describing-coordinate-reference-systems)
- [OGC WKT2 Specification](https://docs.ogc.org/is/12-063r5/12-063r5.html)

---

## Conclusion

This guide provides essential details for working with **custom planetary projections in QGIS**. If you encounter any issues, refer to the respective project links or the [Europlanet GMAP Winter School](https://github.com/europlanet-gmap/winter-school-2025) repository.

Happy Mapping!

