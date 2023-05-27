# QA-activity

import unittest

def div(n1, n2):
    return n1 / n2

class DivTestCase(unittest.TestCase):
    def test_division(self):
        self.assertAlmostEqual(div(10, 2), 5)
        self.assertAlmostEqual(div(7, 3), 2.3333333333333335)
        self.assertAlmostEqual(div(100, 25), 4)

if __name__ == '__main__':
    suite = unittest.TestLoader().loadTestsFromTestCase(DivTestCase)
    unittest.TextTestRunner(verbosity=2).run(suite)
