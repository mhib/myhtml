.PHONY: package
package: ./myhtml-c/lib/static_libmyhtml.a

./myhtml-c:
	git clone https://github.com/lexborisov/myhtml.git ./myhtml-c && cd myhtml-c && git reset --hard fd97a7036c1357578f8c5392de2dd205754cc16a

./myhtml-c/lib/static_libmyhtml.a: ./myhtml-c
	cd myhtml-c && make MyHTML_BUILD_SHARED=OFF MyHTML_BUILD_WITHOUT_THREADS=YES MyHTML_OPTIMIZATION_LEVEL=-O3

.PHONY: clean
clean:
	rm -rf myhtml-c
