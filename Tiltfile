custom_build(
    ref = 'order-service',
    command = './gradlew bootBuildImage --imageName $EXPECTED_REF',
    deps = ['build.gradle', 'src']
)

k8s_yaml([kustomize('k8s')])

k8s_resource('order-service', port_forwards=['9002'])