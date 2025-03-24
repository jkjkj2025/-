<?xml version="1.0" encoding="UTF-8"?>
<definitions xmlns="http://www.omg.org/spec/BPMN/20100524/MODEL" xmlns:bpmndi="http://www.omg.org/spec/BPMN/20100524/DI" xmlns:omgdi="http://www.omg.org/spec/DD/20100524/DI" xmlns:omgdc="http://www.omg.org/spec/DD/20100524/DC" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" id="sid-38422fae-e03e-43a3-bef4-bd33b32041b2" targetNamespace="http://bpmn.io/bpmn" exporter="bpmn-js (https://demo.bpmn.io)" exporterVersion="18.3.1">
  <collaboration id="Collaboration_1hm5cca">
    <participant id="Participant_1xrft9h" name="відділ маркетингу" processRef="Process_1rkt772" />
    <participant id="Participant_1urthm0" name="відділ виробництва/цех" processRef="Process_151dbqs" />
    <participant id="Participant_0vbewm0" name="генеральний директор" processRef="Process_1rj8858" />
    <participant id="Participant_05ueais" name="Розробка нового виробу (від ідеї до установки у виробництво)" />
    <participant id="Participant_0nxap4z" name="технічний відділ" processRef="Process_0mjrzo8" />
    <participant id="Participant_16ni9s1" name="фінансовий відділ" processRef="Process_1jlwsqt" />
    <participant id="Participant_1rmhepd" name="відділ закупівель/склад" processRef="Process_0ir12gv" />
    <messageFlow id="Flow_17k8z7k" sourceRef="Event_08yti39" targetRef="Activity_0vgfl3d" />
    <messageFlow id="Flow_08mpvp8" sourceRef="Event_0ejfrzl" targetRef="Activity_172vo8y" />
    <messageFlow id="Flow_03scwdb" sourceRef="Event_0abqg1g" targetRef="Activity_0rxr05j" />
    <messageFlow id="Flow_1apk7ke" sourceRef="Event_0abqg1g" targetRef="Activity_1c60bqm" />
    <messageFlow id="Flow_09cyrw4" sourceRef="Activity_1wmdq4m" targetRef="Activity_1u1yfji" />
    <messageFlow id="Flow_0r7y616" sourceRef="Activity_0ru5pkp" targetRef="Activity_1wmdq4m" />
    <messageFlow id="Flow_1r5rzqc" sourceRef="Activity_1u1yfji" targetRef="Activity_09eggaw" />
    <messageFlow id="Flow_0p4bwhz" sourceRef="Event_100pgyw" targetRef="Activity_1nfk2ye" />
    <messageFlow id="Flow_1dulxa7" sourceRef="Activity_188ifla" targetRef="Activity_1mvfh2h" />
    <messageFlow id="Flow_0ycvsdw" sourceRef="Activity_1h1hil2" targetRef="Activity_05mffog" />
    <messageFlow id="Flow_0jqbzfn" sourceRef="Activity_0s6amfz" targetRef="Activity_1h1hil2" />
    <messageFlow id="Flow_1vh4zad" sourceRef="Activity_05n9cfx" targetRef="Activity_0vxdba0" />
    <messageFlow id="Flow_08zh06k" sourceRef="Activity_1yb7mjf" targetRef="Activity_0ru5pkp" />
    <messageFlow id="Flow_1opsgcn" sourceRef="Activity_0qjjme5" targetRef="Activity_1nfk2ye" />
    <messageFlow id="Flow_0e5oso9" sourceRef="Activity_07wl59x" targetRef="Activity_07l8o78" />
    <textAnnotation id="TextAnnotation_1pr17oc">
      <text>директор з виробництва</text>
    </textAnnotation>
    <textAnnotation id="TextAnnotation_1ugawau">
      <text>головний технолог</text>
    </textAnnotation>
    <association id="Association_1lb5tsv" associationDirection="None" sourceRef="Activity_05n9cfx" targetRef="TextAnnotation_1pr17oc" />
    <association id="Association_0wxf5vk" associationDirection="None" sourceRef="Activity_05mffog" targetRef="TextAnnotation_1ugawau" />
  </collaboration>
  <process id="Process_1rkt772">
    <task id="Activity_0ru5pkp" name="формування рекомендацій по асортименту та цінам" />
    <startEvent id="Event_1j70hwg">
      <outgoing>Flow_1620ctu</outgoing>
      <outgoing>Flow_0oyeu2w</outgoing>
    </startEvent>
    <task id="Activity_09sa5al" name="збір інформації про ринок">
      <incoming>Flow_1620ctu</incoming>
      <outgoing>Flow_1lqncby</outgoing>
    </task>
    <task id="Activity_1fd138j" name="проведення опитувань клієнтів">
      <incoming>Flow_0oyeu2w</incoming>
      <outgoing>Flow_1wb1002</outgoing>
    </task>
    <intermediateThrowEvent id="Event_08yti39">
      <incoming>Flow_1wb1002</incoming>
      <incoming>Flow_1lqncby</incoming>
    </intermediateThrowEvent>
    <task id="Activity_1u1yfji" name="розробка дизайну нової продукції" />
    <sequenceFlow id="Flow_1620ctu" sourceRef="Event_1j70hwg" targetRef="Activity_09sa5al" />
    <sequenceFlow id="Flow_0oyeu2w" sourceRef="Event_1j70hwg" targetRef="Activity_1fd138j" />
    <sequenceFlow id="Flow_1lqncby" sourceRef="Activity_09sa5al" targetRef="Event_08yti39" />
    <sequenceFlow id="Flow_1wb1002" sourceRef="Activity_1fd138j" targetRef="Event_08yti39" />
  </process>
  <process id="Process_151dbqs">
    <laneSet id="LaneSet_1xfed9c">
      <lane id="Lane_0zog6ie">
        <flowNodeRef>Activity_0vgfl3d</flowNodeRef>
        <flowNodeRef>Activity_0dbybz6</flowNodeRef>
        <flowNodeRef>Activity_1edtff8</flowNodeRef>
        <flowNodeRef>Gateway_0wxii3l</flowNodeRef>
        <flowNodeRef>Activity_05n9cfx</flowNodeRef>
        <flowNodeRef>Activity_172vo8y</flowNodeRef>
        <flowNodeRef>Activity_07czv93</flowNodeRef>
      </lane>
    </laneSet>
    <task id="Activity_0vgfl3d" name="розробка нового продукції">
      <incoming>Flow_1nk51wi</incoming>
      <incoming>Flow_021pjv4</incoming>
      <outgoing>Flow_1xks0mv</outgoing>
    </task>
    <task id="Activity_0dbybz6" name="аналіз можливостей виробництва  продукції">
      <incoming>Flow_1xks0mv</incoming>
      <outgoing>Flow_1szoooh</outgoing>
    </task>
    <task id="Activity_1edtff8" name="причини неможливості виробництва продукції">
      <incoming>Flow_06jmd9b</incoming>
      <outgoing>Flow_1nk51wi</outgoing>
    </task>
    <exclusiveGateway id="Gateway_0wxii3l">
      <incoming>Flow_1szoooh</incoming>
      <outgoing>Flow_0bdhv1t</outgoing>
      <outgoing>Flow_06jmd9b</outgoing>
    </exclusiveGateway>
    <task id="Activity_05n9cfx" name="панування поставки на виробництво нових видів продукції">
      <incoming>Flow_0bdhv1t</incoming>
    </task>
    <task id="Activity_172vo8y" name="перегляд розробки нової продукції">
      <outgoing>Flow_021pjv4</outgoing>
    </task>
    <adHocSubProcess id="Activity_07czv93" name="цех">
      <task id="Activity_0rxr05j" name="підготовка устаткування до роботи">
        <outgoing>Flow_0ibrcsn</outgoing>
      </task>
      <task id="Activity_1nfk2ye" name="надходження сировини на виробництво">
        <outgoing>Flow_0o9d502</outgoing>
      </task>
      <task id="Activity_1h1hil2" name="виготовлення виробу">
        <incoming>Flow_0o9d502</incoming>
        <incoming>Flow_0ibrcsn</incoming>
      </task>
      <sequenceFlow id="Flow_0o9d502" sourceRef="Activity_1nfk2ye" targetRef="Activity_1h1hil2" />
      <task id="Activity_1mvfh2h" name="пакування виробу">
        <outgoing>Flow_016v376</outgoing>
      </task>
      <sequenceFlow id="Flow_0ibrcsn" sourceRef="Activity_0rxr05j" targetRef="Activity_1h1hil2" />
      <task id="Activity_07wl59x" name="відвантаження продукції на склад">
        <incoming>Flow_016v376</incoming>
      </task>
      <sequenceFlow id="Flow_016v376" sourceRef="Activity_1mvfh2h" targetRef="Activity_07wl59x" />
    </adHocSubProcess>
    <sequenceFlow id="Flow_1nk51wi" sourceRef="Activity_1edtff8" targetRef="Activity_0vgfl3d" />
    <sequenceFlow id="Flow_021pjv4" sourceRef="Activity_172vo8y" targetRef="Activity_0vgfl3d" />
    <sequenceFlow id="Flow_1xks0mv" sourceRef="Activity_0vgfl3d" targetRef="Activity_0dbybz6" />
    <sequenceFlow id="Flow_1szoooh" sourceRef="Activity_0dbybz6" targetRef="Gateway_0wxii3l" />
    <sequenceFlow id="Flow_06jmd9b" sourceRef="Gateway_0wxii3l" targetRef="Activity_1edtff8" />
    <sequenceFlow id="Flow_0bdhv1t" sourceRef="Gateway_0wxii3l" targetRef="Activity_05n9cfx" />
  </process>
  <process id="Process_1rj8858">
    <task id="Activity_0vxdba0" name="розгляд нових видів продукції">
      <outgoing>Flow_03szn8z</outgoing>
    </task>
    <exclusiveGateway id="Gateway_1vnrd8x">
      <incoming>Flow_03szn8z</incoming>
      <outgoing>Flow_0vxmmrm</outgoing>
      <outgoing>Flow_0tbi0st</outgoing>
    </exclusiveGateway>
    <intermediateThrowEvent id="Event_0ejfrzl">
      <incoming>Flow_0tbi0st</incoming>
    </intermediateThrowEvent>
    <task id="Activity_1yb7mjf" name="затвердження нових видів продукції">
      <incoming>Flow_0vxmmrm</incoming>
    </task>
    <sequenceFlow id="Flow_03szn8z" sourceRef="Activity_0vxdba0" targetRef="Gateway_1vnrd8x" />
    <sequenceFlow id="Flow_0vxmmrm" sourceRef="Gateway_1vnrd8x" targetRef="Activity_1yb7mjf" />
    <sequenceFlow id="Flow_0tbi0st" sourceRef="Gateway_1vnrd8x" targetRef="Event_0ejfrzl" />
  </process>
  <process id="Process_0mjrzo8">
    <task id="Activity_1wmdq4m" name="розробка нормативів" />
    <task id="Activity_05mffog" name="аналіз якості виготовленої продукції">
      <outgoing>Flow_0buv9hu</outgoing>
    </task>
    <task id="Activity_0s6amfz" name="перевірка виробництва">
      <incoming>Flow_0bnp1a2</incoming>
    </task>
    <exclusiveGateway id="Gateway_13b94x9">
      <incoming>Flow_0buv9hu</incoming>
      <outgoing>Flow_17uk51o</outgoing>
      <outgoing>Flow_0bnp1a2</outgoing>
    </exclusiveGateway>
    <task id="Activity_188ifla" name="оформлення паспортів якості на готову продукцію">
      <incoming>Flow_17uk51o</incoming>
    </task>
    <sequenceFlow id="Flow_0buv9hu" sourceRef="Activity_05mffog" targetRef="Gateway_13b94x9" />
    <sequenceFlow id="Flow_0bnp1a2" sourceRef="Gateway_13b94x9" targetRef="Activity_0s6amfz" />
    <sequenceFlow id="Flow_17uk51o" sourceRef="Gateway_13b94x9" targetRef="Activity_188ifla" />
  </process>
  <process id="Process_1jlwsqt">
    <task id="Activity_09eggaw" name="розрахунок собівартості продукції">
      <outgoing>Flow_0p058ed</outgoing>
    </task>
    <intermediateThrowEvent id="Event_0abqg1g">
      <incoming>Flow_0p058ed</incoming>
    </intermediateThrowEvent>
    <sequenceFlow id="Flow_0p058ed" sourceRef="Activity_09eggaw" targetRef="Event_0abqg1g" />
  </process>
  <process id="Process_0ir12gv">
    <intermediateThrowEvent id="Event_100pgyw">
      <incoming>Flow_0f1zovy</incoming>
    </intermediateThrowEvent>
    <task id="Activity_1c60bqm" name="превірка наявності сировини">
      <outgoing>Flow_0ksygk7</outgoing>
    </task>
    <exclusiveGateway id="Gateway_0s1i0u8">
      <incoming>Flow_0ksygk7</incoming>
      <outgoing>Flow_0ctdtpy</outgoing>
      <outgoing>Flow_0f1zovy</outgoing>
    </exclusiveGateway>
    <task id="Activity_0qjjme5" name="закупівля сировини">
      <incoming>Flow_0ctdtpy</incoming>
    </task>
    <task id="Activity_07l8o78" name="приймання товару">
      <outgoing>Flow_1dbktmb</outgoing>
    </task>
    <task id="Activity_1s4e8c0" name="відвантаження готової продукції">
      <incoming>Flow_1dbktmb</incoming>
      <outgoing>Flow_1b6ibop</outgoing>
    </task>
    <endEvent id="Event_02zddxh">
      <incoming>Flow_1b6ibop</incoming>
    </endEvent>
    <sequenceFlow id="Flow_0f1zovy" sourceRef="Gateway_0s1i0u8" targetRef="Event_100pgyw" />
    <sequenceFlow id="Flow_0ksygk7" sourceRef="Activity_1c60bqm" targetRef="Gateway_0s1i0u8" />
    <sequenceFlow id="Flow_0ctdtpy" sourceRef="Gateway_0s1i0u8" targetRef="Activity_0qjjme5" />
    <sequenceFlow id="Flow_1dbktmb" sourceRef="Activity_07l8o78" targetRef="Activity_1s4e8c0" />
    <sequenceFlow id="Flow_1b6ibop" sourceRef="Activity_1s4e8c0" targetRef="Event_02zddxh" />
  </process>
  <bpmndi:BPMNDiagram id="BpmnDiagram_1">
    <bpmndi:BPMNPlane id="BpmnPlane_1" bpmnElement="Collaboration_1hm5cca">
      <bpmndi:BPMNShape id="Participant_1xrft9h_di" bpmnElement="Participant_1xrft9h" isHorizontal="true">
        <omgdc:Bounds x="160" y="160" width="1190" height="250" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0ru5pkp_di" bpmnElement="Activity_0ru5pkp">
        <omgdc:Bounds x="920" y="240" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_1j70hwg_di" bpmnElement="Event_1j70hwg">
        <omgdc:Bounds x="222" y="262" width="36" height="36" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_09sa5al_di" bpmnElement="Activity_09sa5al">
        <omgdc:Bounds x="310" y="180" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1fd138j_di" bpmnElement="Activity_1fd138j">
        <omgdc:Bounds x="310" y="290" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_08yti39_di" bpmnElement="Event_08yti39">
        <omgdc:Bounds x="472" y="262" width="36" height="36" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1u1yfji_di" bpmnElement="Activity_1u1yfji">
        <omgdc:Bounds x="1150" y="250" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_1620ctu_di" bpmnElement="Flow_1620ctu">
        <omgdi:waypoint x="258" y="280" />
        <omgdi:waypoint x="284" y="280" />
        <omgdi:waypoint x="284" y="220" />
        <omgdi:waypoint x="310" y="220" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0oyeu2w_di" bpmnElement="Flow_0oyeu2w">
        <omgdi:waypoint x="258" y="280" />
        <omgdi:waypoint x="280" y="280" />
        <omgdi:waypoint x="280" y="330" />
        <omgdi:waypoint x="310" y="330" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1lqncby_di" bpmnElement="Flow_1lqncby">
        <omgdi:waypoint x="410" y="220" />
        <omgdi:waypoint x="436" y="220" />
        <omgdi:waypoint x="436" y="280" />
        <omgdi:waypoint x="472" y="280" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1wb1002_di" bpmnElement="Flow_1wb1002">
        <omgdi:waypoint x="410" y="330" />
        <omgdi:waypoint x="441" y="330" />
        <omgdi:waypoint x="441" y="280" />
        <omgdi:waypoint x="472" y="280" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNShape id="Participant_1urthm0_di" bpmnElement="Participant_1urthm0" isHorizontal="true">
        <omgdc:Bounds x="160" y="410" width="2370" height="320" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Lane_0zog6ie_di" bpmnElement="Lane_0zog6ie" isHorizontal="true">
        <omgdc:Bounds x="190" y="410" width="2340" height="320" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0vgfl3d_di" bpmnElement="Activity_0vgfl3d">
        <omgdc:Bounds x="240" y="510" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0dbybz6_di" bpmnElement="Activity_0dbybz6">
        <omgdc:Bounds x="490" y="510" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1edtff8_di" bpmnElement="Activity_1edtff8">
        <omgdc:Bounds x="390" y="420" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_0wxii3l_di" bpmnElement="Gateway_0wxii3l" isMarkerVisible="true">
        <omgdc:Bounds x="635" y="525" width="50" height="50" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_05n9cfx_di" bpmnElement="Activity_05n9cfx">
        <omgdc:Bounds x="750" y="510" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_172vo8y_di" bpmnElement="Activity_172vo8y">
        <omgdc:Bounds x="240" y="630" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0c4f93f_di" bpmnElement="Activity_07czv93" isExpanded="true">
        <omgdc:Bounds x="1360" y="420" width="1060" height="290" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0rxr05j_di" bpmnElement="Activity_0rxr05j">
        <omgdc:Bounds x="1400" y="460" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1nfk2ye_di" bpmnElement="Activity_1nfk2ye">
        <omgdc:Bounds x="1560" y="550" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1h1hil2_di" bpmnElement="Activity_1h1hil2">
        <omgdc:Bounds x="1710" y="480" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1mvfh2h_di" bpmnElement="Activity_1mvfh2h">
        <omgdc:Bounds x="1970" y="580" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_07wl59x_di" bpmnElement="Activity_07wl59x">
        <omgdc:Bounds x="2130" y="580" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_0o9d502_di" bpmnElement="Flow_0o9d502">
        <omgdi:waypoint x="1660" y="590" />
        <omgdi:waypoint x="1685" y="590" />
        <omgdi:waypoint x="1685" y="520" />
        <omgdi:waypoint x="1710" y="520" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0ibrcsn_di" bpmnElement="Flow_0ibrcsn">
        <omgdi:waypoint x="1500" y="500" />
        <omgdi:waypoint x="1605" y="500" />
        <omgdi:waypoint x="1605" y="520" />
        <omgdi:waypoint x="1710" y="520" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_016v376_di" bpmnElement="Flow_016v376">
        <omgdi:waypoint x="2070" y="620" />
        <omgdi:waypoint x="2130" y="620" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1xks0mv_di" bpmnElement="Flow_1xks0mv">
        <omgdi:waypoint x="340" y="550" />
        <omgdi:waypoint x="490" y="550" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1szoooh_di" bpmnElement="Flow_1szoooh">
        <omgdi:waypoint x="590" y="550" />
        <omgdi:waypoint x="635" y="550" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0bdhv1t_di" bpmnElement="Flow_0bdhv1t">
        <omgdi:waypoint x="685" y="550" />
        <omgdi:waypoint x="750" y="550" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_06jmd9b_di" bpmnElement="Flow_06jmd9b">
        <omgdi:waypoint x="660" y="525" />
        <omgdi:waypoint x="660" y="460" />
        <omgdi:waypoint x="490" y="460" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1nk51wi_di" bpmnElement="Flow_1nk51wi">
        <omgdi:waypoint x="390" y="460" />
        <omgdi:waypoint x="365" y="460" />
        <omgdi:waypoint x="365" y="520" />
        <omgdi:waypoint x="340" y="520" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_021pjv4_di" bpmnElement="Flow_021pjv4">
        <omgdi:waypoint x="290" y="630" />
        <omgdi:waypoint x="290" y="590" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNShape id="Participant_0vbewm0_di" bpmnElement="Participant_0vbewm0" isHorizontal="true">
        <omgdc:Bounds x="160" y="730" width="910" height="180" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0vxdba0_di" bpmnElement="Activity_0vxdba0">
        <omgdc:Bounds x="480" y="750" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_1vnrd8x_di" bpmnElement="Gateway_1vnrd8x" isMarkerVisible="true">
        <omgdc:Bounds x="665" y="765" width="50" height="50" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_0ejfrzl_di" bpmnElement="Event_0ejfrzl">
        <omgdc:Bounds x="272" y="842" width="36" height="36" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1yb7mjf_di" bpmnElement="Activity_1yb7mjf">
        <omgdc:Bounds x="780" y="750" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_03szn8z_di" bpmnElement="Flow_03szn8z">
        <omgdi:waypoint x="580" y="790" />
        <omgdi:waypoint x="665" y="790" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0vxmmrm_di" bpmnElement="Flow_0vxmmrm">
        <omgdi:waypoint x="715" y="790" />
        <omgdi:waypoint x="780" y="790" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0tbi0st_di" bpmnElement="Flow_0tbi0st">
        <omgdi:waypoint x="690" y="815" />
        <omgdi:waypoint x="690" y="860" />
        <omgdi:waypoint x="308" y="860" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNShape id="Participant_0nxap4z_di" bpmnElement="Participant_0nxap4z" isHorizontal="true">
        <omgdc:Bounds x="1020" y="910" width="1220" height="210" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1wmdq4m_di" bpmnElement="Activity_1wmdq4m">
        <omgdc:Bounds x="1120" y="950" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_05mffog_di" bpmnElement="Activity_05mffog">
        <omgdc:Bounds x="1690" y="1010" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0s6amfz_di" bpmnElement="Activity_0s6amfz">
        <omgdc:Bounds x="1810" y="920" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_13b94x9_di" bpmnElement="Gateway_13b94x9" isMarkerVisible="true">
        <omgdc:Bounds x="1905" y="1025" width="50" height="50" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_188ifla_di" bpmnElement="Activity_188ifla">
        <omgdc:Bounds x="2020" y="1010" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_17uk51o_di" bpmnElement="Flow_17uk51o">
        <omgdi:waypoint x="1955" y="1050" />
        <omgdi:waypoint x="2020" y="1050" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0bnp1a2_di" bpmnElement="Flow_0bnp1a2">
        <omgdi:waypoint x="1930" y="1025" />
        <omgdi:waypoint x="1930" y="960" />
        <omgdi:waypoint x="1910" y="960" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0buv9hu_di" bpmnElement="Flow_0buv9hu">
        <omgdi:waypoint x="1790" y="1050" />
        <omgdi:waypoint x="1905" y="1050" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNShape id="Participant_16ni9s1_di" bpmnElement="Participant_16ni9s1" isHorizontal="true">
        <omgdc:Bounds x="1190" y="1120" width="320" height="160" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_09eggaw_di" bpmnElement="Activity_09eggaw">
        <omgdc:Bounds x="1280" y="1150" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_0abqg1g_di" bpmnElement="Event_0abqg1g">
        <omgdc:Bounds x="1432" y="1172" width="36" height="36" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_0p058ed_di" bpmnElement="Flow_0p058ed">
        <omgdi:waypoint x="1380" y="1190" />
        <omgdi:waypoint x="1432" y="1190" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNShape id="Participant_1rmhepd_di" bpmnElement="Participant_1rmhepd" isHorizontal="true">
        <omgdc:Bounds x="1330" y="1280" width="1200" height="278" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_100pgyw_di" bpmnElement="Event_100pgyw">
        <omgdc:Bounds x="1572" y="1292" width="36" height="36" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1c60bqm_di" bpmnElement="Activity_1c60bqm">
        <omgdc:Bounds x="1410" y="1340" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_0s1i0u8_di" bpmnElement="Gateway_0s1i0u8" isMarkerVisible="true">
        <omgdc:Bounds x="1565" y="1355" width="50" height="50" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0qjjme5_di" bpmnElement="Activity_0qjjme5">
        <omgdc:Bounds x="1490" y="1450" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_07l8o78_di" bpmnElement="Activity_07l8o78">
        <omgdc:Bounds x="2130" y="1330" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1s4e8c0_di" bpmnElement="Activity_1s4e8c0">
        <omgdc:Bounds x="2260" y="1440" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_02zddxh_di" bpmnElement="Event_02zddxh">
        <omgdc:Bounds x="2432" y="1462" width="36" height="36" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_0f1zovy_di" bpmnElement="Flow_0f1zovy">
        <omgdi:waypoint x="1590" y="1355" />
        <omgdi:waypoint x="1590" y="1328" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0ksygk7_di" bpmnElement="Flow_0ksygk7">
        <omgdi:waypoint x="1510" y="1380" />
        <omgdi:waypoint x="1565" y="1380" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0ctdtpy_di" bpmnElement="Flow_0ctdtpy">
        <omgdi:waypoint x="1590" y="1405" />
        <omgdi:waypoint x="1590" y="1428" />
        <omgdi:waypoint x="1540" y="1428" />
        <omgdi:waypoint x="1540" y="1450" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1dbktmb_di" bpmnElement="Flow_1dbktmb">
        <omgdi:waypoint x="2180" y="1410" />
        <omgdi:waypoint x="2180" y="1480" />
        <omgdi:waypoint x="2260" y="1480" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1b6ibop_di" bpmnElement="Flow_1b6ibop">
        <omgdi:waypoint x="2360" y="1480" />
        <omgdi:waypoint x="2432" y="1480" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNShape id="Participant_05ueais_di" bpmnElement="Participant_05ueais" isHorizontal="true">
        <omgdc:Bounds x="440" y="80" width="610" height="60" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Association_1lb5tsv_di" bpmnElement="Association_1lb5tsv">
        <omgdi:waypoint x="800" y="510" />
        <omgdi:waypoint x="800" y="490" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Association_0wxf5vk_di" bpmnElement="Association_0wxf5vk">
        <omgdi:waypoint x="1724" y="1010" />
        <omgdi:waypoint x="1716" y="990" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_17k8z7k_di" bpmnElement="Flow_17k8z7k">
        <omgdi:waypoint x="490" y="298" />
        <omgdi:waypoint x="490" y="390" />
        <omgdi:waypoint x="290" y="390" />
        <omgdi:waypoint x="290" y="510" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNShape id="TextAnnotation_1pr17oc_di" bpmnElement="TextAnnotation_1pr17oc">
        <omgdc:Bounds x="750" y="450" width="99.99999794078421" height="40.48582995951417" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_08mpvp8_di" bpmnElement="Flow_08mpvp8">
        <omgdi:waypoint x="290" y="842" />
        <omgdi:waypoint x="290" y="710" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_03scwdb_di" bpmnElement="Flow_03scwdb">
        <omgdi:waypoint x="1450" y="1172" />
        <omgdi:waypoint x="1450" y="540" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1apk7ke_di" bpmnElement="Flow_1apk7ke">
        <omgdi:waypoint x="1450" y="1208" />
        <omgdi:waypoint x="1450" y="1340" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_09cyrw4_di" bpmnElement="Flow_09cyrw4">
        <omgdi:waypoint x="1200" y="950" />
        <omgdi:waypoint x="1200" y="330" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0r7y616_di" bpmnElement="Flow_0r7y616">
        <omgdi:waypoint x="1020" y="280" />
        <omgdi:waypoint x="1110" y="280" />
        <omgdi:waypoint x="1110" y="635" />
        <omgdi:waypoint x="1150" y="635" />
        <omgdi:waypoint x="1150" y="950" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1r5rzqc_di" bpmnElement="Flow_1r5rzqc">
        <omgdi:waypoint x="1250" y="290" />
        <omgdi:waypoint x="1290" y="290" />
        <omgdi:waypoint x="1290" y="705" />
        <omgdi:waypoint x="1320" y="705" />
        <omgdi:waypoint x="1320" y="1150" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0p4bwhz_di" bpmnElement="Flow_0p4bwhz">
        <omgdi:waypoint x="1590" y="1292" />
        <omgdi:waypoint x="1590" y="630" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1dulxa7_di" bpmnElement="Flow_1dulxa7">
        <omgdi:waypoint x="2040" y="1010" />
        <omgdi:waypoint x="2040" y="660" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0ycvsdw_di" bpmnElement="Flow_0ycvsdw">
        <omgdi:waypoint x="1730" y="560" />
        <omgdi:waypoint x="1730" y="1010" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0jqbzfn_di" bpmnElement="Flow_0jqbzfn">
        <omgdi:waypoint x="1860" y="920" />
        <omgdi:waypoint x="1860" y="815" />
        <omgdi:waypoint x="1780" y="815" />
        <omgdi:waypoint x="1780" y="560" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNShape id="TextAnnotation_1ugawau_di" bpmnElement="TextAnnotation_1ugawau">
        <omgdc:Bounds x="1660" y="960" width="100" height="30" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_1vh4zad_di" bpmnElement="Flow_1vh4zad">
        <omgdi:waypoint x="800" y="590" />
        <omgdi:waypoint x="800" y="670" />
        <omgdi:waypoint x="530" y="670" />
        <omgdi:waypoint x="530" y="750" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_08zh06k_di" bpmnElement="Flow_08zh06k">
        <omgdi:waypoint x="880" y="790" />
        <omgdi:waypoint x="980" y="790" />
        <omgdi:waypoint x="980" y="320" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1opsgcn_di" bpmnElement="Flow_1opsgcn">
        <omgdi:waypoint x="1590" y="1490" />
        <omgdi:waypoint x="1640" y="1490" />
        <omgdi:waypoint x="1640" y="630" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0e5oso9_di" bpmnElement="Flow_0e5oso9">
        <omgdi:waypoint x="2180" y="660" />
        <omgdi:waypoint x="2180" y="1330" />
      </bpmndi:BPMNEdge>
    </bpmndi:BPMNPlane>
  </bpmndi:BPMNDiagram>
</definitions>
