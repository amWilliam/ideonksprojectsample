# Fibonacci
def fibonacci(n):
    """Generate Fibonacci series up to n terms."""
    fib_series = [0, 1]
    while fib_series[-1] + fib_series[-2] <= n:
        fib_series.append(fib_series[-1] + fib_series[-2])
    return fib_series
    
# Import
import unittest
from fibonacci_generator import fibonacci

# Classification
class TestFibonacci(unittest.TestCase):
    def test_fibonacci(self):
        self.assertEqual(fibonacci(5), [0, 1, 1, 2, 3, 5])
        self.assertEqual(fibonacci(10), [0, 1, 1, 2, 3, 5, 8])
        self.assertEqual(fibonacci(50), [0, 1, 1, 2, 3, 5, 8, 13, 21, 34])
        self.assertEqual(fibonacci(100), [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89])
        self.assertEqual(fibonacci(1000), [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610, 987])
        
# If function
if __name__ == '__main__':
    unittest.main()

# Fibonacci Generator

A Python package to generate Fibonacci series up to n terms.

## Installation

You can install `fibonacci_generator` via pip:


```python
from setuptools import setup, find_packages

setup(
    name='fibonacci_generator',
    version='0.1',
    packages=find_packages(),
    license='MIT',
    description='A Python package to generate Fibonacci series up to n terms.',
    long_description=open('README.md').read(),
    long_description_content_type='text/markdown',
    author='Your Name',
    author_email='your@email.com',
    url='https://github.com/yourusername/fibonacci-generator',
    keywords=['fibonacci', 'generator', 'sequence'],
    classifiers=[
        'Development Status :: 3 - Alpha',
        'Intended Audience :: Developers',
        'License :: OSI Approved :: MIT License',
        'Programming Language :: Python :: 3',
        'Programming Language :: Python :: 3.6',
        'Programming Language :: Python :: 3.7',
        'Programming Language :: Python :: 3.8',
        'Programming Language :: Python :: 3.9',
    ],
)
