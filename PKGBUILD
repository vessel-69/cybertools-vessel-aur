# Maintainer: vessel-69 <vessel@cyber-tools.dev>

pkgname=cybertools-vessel
pkgver=2.0.0
pkgrel=1
pkgdesc="Global CLI for CyberTools API — recon, subdomain enum, payload gen for bug bounty hunters"
arch=('any')
url="https://github.com/vessel-69/cybertools-vessel"
license=('MIT')
depends=('python>=3.10')
makedepends=('python-build' 'python-installer' 'python-wheel' 'python-setuptools')
source=("https://files.pythonhosted.org/packages/source/c/cybertools-vessel/cybertools_vessel-${pkgver}.tar.gz")
sha256sums=('SKIP')  # update with: sha256sum cybertools_vessel-2.0.0.tar.gz

build() {
    cd "cybertools_vessel-${pkgver}"
    python -m build --wheel --no-isolation
}

package() {
    cd "cybertools_vessel-${pkgver}"
    python -m installer --destdir="$pkgdir" dist/*.whl

    # Install license
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
