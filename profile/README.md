<p align="center"><img src="https://raw.githubusercontent.com/go-approx/brand/main/social/go-approx.png" alt="go-approx" width="720"></p>

# go-approx

🌐 **[Website](https://go-approx.github.io)** · 📚 **[Documentation](https://go-approx.github.io/docs/)**

**Interpolation, splines and polynomials in pure Go (CGO=0), validated against SciPy and NumPy.**

`interp` provides the interpolators of `scipy.interpolate` (1-D and N-D,
cubic, PCHIP, Akima, B-splines, FITPACK smoothing splines) and `poly` the
polynomial tools of NumPy (`polyfit`, `roots`, the `numpy.polynomial` bases).
Both run SciPy and NumPy as oracles and compare to them value by value.
Chebyshev and AAA rational approximation are planned.

```go
s, _ := interp.NewCubicSpline(x, y, "not-a-knot")
v := s.At(2.5)

fit, _ := poly.Polyfit(x, y, 3, nil)
r, _ := poly.Roots(fit.Coef)
```

## Repositories

| Repo | What it is | Status |
|------|------------|--------|
| [**interp**](https://github.com/go-approx/interp) | interpolation, splines and smoothing: `interp1d`, cubic, PCHIP, Akima, B-splines, FITPACK smoothing splines, regular-grid and tensor-product interpolation | released v0.1.0 |
| [**poly**](https://github.com/go-approx/poly) | polynomials: evaluation, arithmetic, least-squares fits, roots, and the Chebyshev, Legendre, Hermite, HermiteE and Laguerre bases | released v0.1.0 |
| [**docs**](https://github.com/go-approx/docs) | the documentation site (Hugo + Hextra), served at [/docs/](https://go-approx.github.io/docs/) | |
| [**go-approx.github.io**](https://github.com/go-approx/go-approx.github.io) | the landing page (Hugo) | |
| [**brand**](https://github.com/go-approx/brand) | logo, icons and social images | |
