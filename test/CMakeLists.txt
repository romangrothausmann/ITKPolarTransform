itk_module_test()

set(PolarTransformTests
  itkPolarTransformTest.cxx
  )

CreateTestDriver(PolarTransform "${PolarTransform-Test_LIBRARIES}" "${PolarTransformTests}")

itk_add_test(NAME itkPolarTransformTest
  COMMAND PolarTransformTestDriver itkPolarTransformTest
  )

itk_python_expression_add_test(NAME itkPolarToCartesianTransformPythonTest
  EXPRESSION "instance = itk.PolarToCartesianTransform.New()")
itk_python_expression_add_test(NAME itkCartesianToPolarTransformPythonTest
  EXPRESSION "instance = itk.CartesianToPolarTransform.New()")
