# Additional images:
    - quay.io/integreatly/prometheus-blackbox-exporter@sha256:35b9d2c1002201723b7f7a9f54e9406b2ec4b5b0f73d114f47c70e15956103b5
    - quay.io/modh/cuda-notebooks@sha256:2163ba74f602ec4b3049a88dcfa4fe0a8d0fff231090001947da66ef8e75ab9a
    - quay.io/modh/cuda-notebooks@sha256:25d7e3318850dff7e91c1451cdd7256e78b02f4a1f6d17a37d6c2797923ce4b6
    - quay.io/modh/cuda-notebooks@sha256:2c177921d08563abffc8711b965e4c617aca243146cb4b43ec409a466be10a13
    - quay.io/modh/cuda-notebooks@sha256:348fa993347f86d1e0913853fb726c584ae8b5181152f0430967d380d68d804f
    - quay.io/modh/cuda-notebooks@sha256:492c37fb4b71c07d929ac7963896e074871ded506230fe926cdac21eb1ab9db8
    - quay.io/modh/odh-anaconda-notebook@sha256:380c07bf79f5ec7d22441cde276c50b5eb2a459485cde05087837639a566ae3d
    - quay.io/modh/odh-generic-data-science-notebook@sha256:ebb5613e6b53dc4e8efcfe3878b4cd10ccb77c67d12c00d2b8c9d41aeffd7df5
    - quay.io/modh/odh-generic-data-science-notebook@sha256:f1c285f88f37abb0d54efc1941f349dfed824896568bcd359770e15d78fdb9f9
    - quay.io/modh/odh-minimal-notebook-container@sha256:0f7ca48f669a45ce25dc0df4bd89ba7b490f44654d5efa92fc0a20b4899e82ef
    - quay.io/modh/odh-minimal-notebook-container@sha256:a5a7738b09a204804e084a45f96360b568b0b9d85709c0ce6742d440ff917183
    - quay.io/modh/odh-pytorch-notebook@sha256:5e1523a2637beb5f9d3a2aaca65a18febe1b2e08e5e8a724596c38554a317b8a
    - quay.io/modh/odh-trustyai-notebook@sha256:83fa3b34eb237bb7716ac1e021f7b123099574765546f0c450ab06c43df34ad9
    - quay.io/opendatahub/openvino_model_server@sha256:20dbfbaf53d1afbd47c612d953984238cb0e207972ed544a5ea662c2404f276d
    - quay.io/modh/must-gather@sha256:c2d780156a0e7cec975c9c150bee00b1facb8f6213e7b98a7a489448d76dfd94
    - quay.io/modh/runtime-images@sha256:03e0f71042dad9953f49e57c2f547ea8ac346feffcee5cc5f1c47c530174afcf
    - quay.io/modh/runtime-images@sha256:7ca2509fa522cb38720a8d30f19077a1f5acefa8be2801ee541b8fc8731daf84
    - quay.io/modh/runtime-images@sha256:7dd23e58291cad7a0ab4a8e04bda06492f2c027eb33b226358380db58dcdd60b
    - quay.io/modh/runtime-images@sha256:8b962c575adfdb46a9aa3e3fc30fdbe470d049b0ff69f68c5c9f950496ae26c5
    - quay.io/modh/runtime-images@sha256:8df90db22b29afb1cd9c81d52be9145fed50e3b04ec80bb7ea7ecaa7476dbe5c
    - quay.io/modh/runtime-images@sha256:c775356ad2efcb59e151cef57dab48cabc9f12e3c69f1453bcb768eabb950cbf
    - quay.io/modh/runtime-images@sha256:cb54fa7c48b2bbca0e173470330ea37efa6d5dd0acd015ac8a0230aa31661eba
    - quay.io/modh/runtime-images@sha256:cccbf0b9c85921578853211c3a2857e68f3cf856cfc59af7268afe2948eb19a6

# ImageSetConfiguration example:
```yaml
kind: ImageSetConfiguration
apiVersion: mirror.openshift.io/v1alpha2
archiveSize: 4
storageConfig:
  registry: 
    imageURL: registry.example.com:5000/mirror/oc-mirror-metadata
    skipTLS: false                       
mirror:
  operators:
  - catalog: registry.redhat.io/redhat/redhat-operator-index:v4.13
    packages:
    - name: rhods-operator
      channels:
      - name: stable
  additionalImages:   
    - name: quay.io/integreatly/prometheus-blackbox-exporter@sha256:35b9d2c1002201723b7f7a9f54e9406b2ec4b5b0f73d114f47c70e15956103b5
    - name: quay.io/modh/cuda-notebooks@sha256:2163ba74f602ec4b3049a88dcfa4fe0a8d0fff231090001947da66ef8e75ab9a
    - name: quay.io/modh/cuda-notebooks@sha256:25d7e3318850dff7e91c1451cdd7256e78b02f4a1f6d17a37d6c2797923ce4b6
    - name: quay.io/modh/cuda-notebooks@sha256:2c177921d08563abffc8711b965e4c617aca243146cb4b43ec409a466be10a13
    - name: quay.io/modh/cuda-notebooks@sha256:348fa993347f86d1e0913853fb726c584ae8b5181152f0430967d380d68d804f
    - name: quay.io/modh/cuda-notebooks@sha256:492c37fb4b71c07d929ac7963896e074871ded506230fe926cdac21eb1ab9db8
    - name: quay.io/modh/odh-anaconda-notebook@sha256:380c07bf79f5ec7d22441cde276c50b5eb2a459485cde05087837639a566ae3d
    - name: quay.io/modh/odh-generic-data-science-notebook@sha256:ebb5613e6b53dc4e8efcfe3878b4cd10ccb77c67d12c00d2b8c9d41aeffd7df5
    - name: quay.io/modh/odh-generic-data-science-notebook@sha256:f1c285f88f37abb0d54efc1941f349dfed824896568bcd359770e15d78fdb9f9
    - name: quay.io/modh/odh-minimal-notebook-container@sha256:0f7ca48f669a45ce25dc0df4bd89ba7b490f44654d5efa92fc0a20b4899e82ef
    - name: quay.io/modh/odh-minimal-notebook-container@sha256:a5a7738b09a204804e084a45f96360b568b0b9d85709c0ce6742d440ff917183
    - name: quay.io/modh/odh-pytorch-notebook@sha256:5e1523a2637beb5f9d3a2aaca65a18febe1b2e08e5e8a724596c38554a317b8a
    - name: quay.io/modh/odh-trustyai-notebook@sha256:83fa3b34eb237bb7716ac1e021f7b123099574765546f0c450ab06c43df34ad9
    - name: quay.io/opendatahub/openvino_model_server@sha256:20dbfbaf53d1afbd47c612d953984238cb0e207972ed544a5ea662c2404f276d
    - name: quay.io/modh/runtime-images@sha256:03e0f71042dad9953f49e57c2f547ea8ac346feffcee5cc5f1c47c530174afcf
    - name: quay.io/modh/runtime-images@sha256:7ca2509fa522cb38720a8d30f19077a1f5acefa8be2801ee541b8fc8731daf84
    - name: quay.io/modh/runtime-images@sha256:7dd23e58291cad7a0ab4a8e04bda06492f2c027eb33b226358380db58dcdd60b
    - name: quay.io/modh/runtime-images@sha256:8b962c575adfdb46a9aa3e3fc30fdbe470d049b0ff69f68c5c9f950496ae26c5
    - name: quay.io/modh/runtime-images@sha256:8df90db22b29afb1cd9c81d52be9145fed50e3b04ec80bb7ea7ecaa7476dbe5c
    - name: quay.io/modh/runtime-images@sha256:c775356ad2efcb59e151cef57dab48cabc9f12e3c69f1453bcb768eabb950cbf
    - name: quay.io/modh/runtime-images@sha256:cb54fa7c48b2bbca0e173470330ea37efa6d5dd0acd015ac8a0230aa31661eba
    - name: quay.io/modh/runtime-images@sha256:cccbf0b9c85921578853211c3a2857e68f3cf856cfc59af7268afe2948eb19a6
    - name: quay.io/modh/must-gather@sha256:c2d780156a0e7cec975c9c150bee00b1facb8f6213e7b98a7a489448d76dfd94
```
