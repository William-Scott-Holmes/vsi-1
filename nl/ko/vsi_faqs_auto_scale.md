---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# FAQ: 자동 스케일링
{: #faqs-auto-scale}

## 자동 스케일링은 베어메탈 자동 스케일링 인스턴스를 지원합니까?
{: faq}

현재 자동 스케일링은 베어메탈 자동 스케일링 인스턴스를 지원하지 않습니다.

## 자동 스케일링은 로드 밸런서에서 작동합니까?
{: faq}

네, 자동 스케일링은 현재 로드 밸런서에서 작동하며 로드 밸런서 API의 일부를 사용합니다. 자세한 정보는 [로드 밸런서 스케일링](/docs/vsi?topic=virtual-servers-auto-scale-terminology)을 참조하십시오.

## 다른 자동 스케일링 종료 정책은 무엇입니까?
{: faq}

최신, 이전 및 다음 비용 청구가 가장 임박의 세 가지 자동 스케일링 종료 정책이 있습니다. 축소할 때 그룹이 제거할 멤버를 선택하는 방법에 대해 설명합니다. 자세한 정보는 [종료 정책](/docs/vsi?topic=virtual-servers-auto-scale-terminology)을 참조하십시오.

## 자동 스케일링 정책은 무엇입니까?
{: faq}

정책은 조치 세트 및 트리거 세트를 보유합니다. 일반적으로 정책은 이름, 쿨다운, 조치 및 트리거와 같은 요소로 구성됩니다. 자세한 정보는 [정책](/docs/vsi?topic=virtual-servers-auto-scale-terminology)을 참조하십시오.

## 자동 스케일링 트리거는 무엇입니까?
{: faq}

트리거는 충족될 수 있는 조건입니다(그룹이 활성 상태인 경우에만). 트리거에는 일회성, 반복 및 리소스 사용의 세 가지 유형이 있습니다. 자세한 정보는 [트리거](/docs/vsi?topic=virtual-servers-auto-scale-terminology)를 참조하십시오.

## 최대 VSI 멤버 수는 얼마나 됩니까?
{: faq}

그룹에서 허용하는 최대 멤버입니다. 자세한 정보는 [최대 VSI 멤버 수](/docs/vsi?topic=virtual-servers-auto-scale-terminology)를 참조하십시오.

## 최소 VSI 멤버 수는 얼마나 됩니까?
{: faq}

그룹에서 허용하는 최소 멤버입니다. 자세한 정보는 [최소 VSI 멤버 수](/docs/vsi?topic=virtual-servers-auto-scale-terminology)를 참조하십시오.

## 자동 스케일링 자산은 무엇입니까?
{: faq}

자산은 멤버 수에 기여하지 않는 그룹의 고정된 멤버이며 어떠한 방법으로도 자동으로 제어되지 않습니다. 자산은 정책 트리거에 추가 정보를 제공하기 위해 존재합니다. 예를 들어, 자산은 CPU 백분율이 트리거로 사용되는 경우 전체 그룹 CPU 백분율에 기여할 수 있습니다. 현재 그룹에는 가상 게스트 자산만 있을 수 있으며 수에는 제한이 없습니다. 또한 그룹은 필요하지 않습니다. 

## 자동 스케일링 그룹은 무엇입니까?
{: faq}

그룹(스케일링 그룹)은 자산, 멤버, 스케일링 로드 밸런서, VLAN 및 정책의 그룹별 콜렉션입니다. 그룹에는 멤버 수 경계와 스케일링된 가상 서버 인스턴스 수 템플리트를 포함하여 스케일링을 위한 모든 매개변수가 있습니다. 

## 자동 스케일링 멤버는 무엇입니까?
{: faq}

멤버는 그룹에서 스케일링된 단위입니다. 멤버는 자동으로 프로비저닝되거나 정책 조치에 따라 재확보됩니다. 현재 모든 멤버는 가상 서버 인스턴스입니다. 활성 그룹에서 최소값보다 적거나 최대값보다 많은 멤버는 없습니다. 일반적으로 멤버는 정책 조치로 추가되지만 사용자가 수동으로 추가할 수도 있습니다. 