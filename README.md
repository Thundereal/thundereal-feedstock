About thundereal-feedstock
==========================

Feedstock license: [BSD-3-Clause](https://github.com/realthunder/thundereal-feedstock/blob/main/LICENSE.txt)

Home: https://github.com/realthunder/FreeCAD

Package license: LGPL2

Summary: Thundereal CAD, a parametric 3D modeler forked from FreeCAD

Thundereal CAD, the realthunder fork of FreeCAD (the Link branch)
with its own app id and artwork.


Current build status
====================


<table><tr>
    <td>GitHub Actions</td>
    <td>
      <a href="https://github.com/realthunder/thundereal-feedstock/actions/workflows/conda-build.yml">
        <img src="https://github.com/realthunder/thundereal-feedstock/actions/workflows/conda-build.yml/badge.svg?event=push&branch=main">
      </a>
    </td>
  </tr>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-thundereal-green.svg)](https://anaconda.org/realthunder/thundereal) | [![Conda Downloads](https://img.shields.io/conda/dn/realthunder/thundereal.svg)](https://anaconda.org/realthunder/thundereal) | [![Conda Version](https://img.shields.io/conda/vn/realthunder/thundereal.svg)](https://anaconda.org/realthunder/thundereal) | [![Conda Platforms](https://img.shields.io/conda/pn/realthunder/thundereal.svg)](https://anaconda.org/realthunder/thundereal) |

Installing thundereal
=====================

Installing `thundereal` from the `realthunder` channel can be achieved by adding `realthunder` to your channels with:

```
conda config --add channels realthunder
```

Leave `channel_priority` at its default, `flexible`. **Do not set it to
`strict`** (the line this README used to carry): `occt`, `smesh`,
`ifcopenshell` and `gmsh` are names conda-forge has too, and the package
needs the realthunder builds of the first three. `conda` solves that either
way. `mamba` 2.9 with the `.condarc` Miniforge ships -- the one with a
`mirrored_channels` block for conda-forge -- ranks conda-forge above
realthunder whatever the order given, so under `strict` it finds nothing to
install, and under `flexible` it used to take conda-forge's upstream `occt`.
The package now names the builds it needs, so `flexible` gets them with
either tool. This section is written by hand: a `conda smithy rerender`
puts the old line back, and it has to be taken out again.

How to use
----------

<details>
<summary>With conda</summary>

```
conda install thundereal
```

</details>

<details>
<summary>With mamba</summary>

```
mamba install thundereal
```

</details>

<details>
<summary>With pixi</summary>

```
# for adding to your local project
pixi add thundereal
# for installing globally
pixi global install thundereal
```

</details>

Search package versions
-----------------------

It is possible to list all of the versions of `thundereal` available on your platform:

<details>
<summary>With conda</summary>

```
conda search thundereal --channel realthunder
```

</details>

<details>
<summary>With mamba</summary>

```
mamba search thundereal --channel realthunder
```

</details>

<details>
<summary>With pixi</summary>

```
pixi search thundereal --channel realthunder
```

</details>

<details>
<summary>With mamba repoquery, which may provide more information</summary>

```
# Search all versions available on your platform:
mamba repoquery search thundereal --channel realthunder

# List packages depending on `thundereal`:
mamba repoquery whoneeds thundereal --channel realthunder

# List dependencies of `thundereal`:
mamba repoquery depends thundereal --channel realthunder
```

</details>




Updating thundereal-feedstock
=============================

If you would like to improve the thundereal recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`realthunder` channel, whereupon the built conda packages will be available for
everybody to install and use from the `realthunder` channel.
Note that all branches in the realthunder/thundereal-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks, and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@realthunder](https://github.com/realthunder/)

